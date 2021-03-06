CSS Layout position property

### positioning behaviour can be understood using top/bottom or left/right

1. static  : 

        by default all css elements has static positioning. this position will follow just normal flow. 
        setting top/bottom or left/right will not affect position of element. 
        
        
2. relative : 

        if a element is set with relative, setting top/bottom or left/right will move element from its original position. 
        if you set top : 100px, element will move below from its original position.
        if you set bottom : 100px, element will move above/upside from its orginal position.
        there is no question of parent container because, element always moves with respect to its original/normal postion, it doesn't care parents position.

style.css

        .samplebox {
          height: 100px;
          width: 100px;
          border-style: solid;
          border-width: 2px;
          border-color: red;
          position: relative;
          bottom: 100px;      /*you can see box moving top from its original position. imagine xy co-ordinate plane*/
        }
        
        
index.html
        
             <!DOCTYPE html>
                <body>
                  <p>hello hellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohello</p>
                  <div class="samplebox"></div>
                  <p>hello hellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohellohello</p>
                </body>
             </html>
        
        
3. absolute :

          setting absolute to an element makes it come out of normal flow , below element will take its place.
          setting top/bottom left/right moves absolute element with respect to context of parent element(with position property) or context of screen.
          
          .samplebox {
              height: 100px;
              width: 100px;
              border-style: solid;
              border-width: 2px;
              border-color: red;
              position: absolute;
            }
            
            if you set top/bottom or left/right, it starts moving with respect to original/normal position of parent element(parent element must have position property).
            if there is no parent element(with position property), then body will be considered as parent element.
            so parent container plays important role(with position property). 
            For absolute position, check whether there is a parent(with position property) or screen(document body itself)
            
            .samplebox {
              height: 100px;
              width: 100px;
              border-style: solid;
              border-width: 2px;
              border-color: red;
              position: absolute;
              top: 10px;      /*you can see this box will move to x:10px, y:10px position ,top right corner of body(body is the parent if no parent exists)*/
              right: 10px;
            }



4. fixed : 

          if element is set its property as fixed, it will come out of normal flow(till now same as absolute).
          fixed positiion element will stays in same position if you scroll screen. but absolute position move with scroll.
          fixed will always consider its parent as screen body. if you set top/bottom or left/right, it will move with respect to screen/viewport/body.
          even if you put parent element for fixed ,it doesn't care, it consider viewport as parent.

          .samplebox {
            height: 100px;
            width: 100px;
            border-style: solid;
            border-width: 2px;
            border-color: red;
            position: fixed;
            top: 0px;
            right: 0px;
          }


5. sticky : 
   
   behaves as combination of relative and fixed.
   when u scroll the page, element will move until it reaches the position(example top 20px). when it reaches top 20px. 
   when element reaches position, its position becomes fixed.
   
   1. case : parent container is viewport(screen) : sticky element position will be fixed after reaching top/bottom or left/right position
   2. case : parent container is another container(div) : sticky element position will be fixed till parent container visible on screent.
                onscroll if parent container disappears then sticky element also scrolled up along with parent and disappear.
   
   
           .samplebox {
                  height: 100px;
                  width: 100px;
                  border-style: solid;
                  border-width: 2px;
                  border-color: red;
                  position: sticky;
                  top: 20px;    /* element will scroll as long as its distance is >= 20px from top, when it reaches 20px from top, it stops scrolling */
                }

### links 

https://learn.shayhowe.com/advanced-html-css/detailed-css-positioning/
