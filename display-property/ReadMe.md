
inline : takes width equal to content, if you try to set height and width, they are ignored.  
block : takes full line, you can set height and width to element.  
inline-block : normarlly inline element ignores height and width, but you can set height and width to inline-block element.   
none : element will be hidden from view but can be seen in dom.  

inline-block: important : you can use this property to bring two inline or block elements in same line and partition the screen. but bootstrap has better solution.

        .left {
          width : 30%;
          background-color: yellow;
          height: 100%;
          display: inline-block;
        }

        .right {
          width : 60%; 
          background-color: red;
          height: 100%;
          display: inline-block;
        }

        body {
          height: 100%;
        }

        html {
          height: 100%;
        }

#### display none vs visiblity hidden : 

display: none;  - 

                this value removes the element to which you apply it from the document flow. 
                This means that the element is not visible and it also doesn't "block its position". 
                Other elements can (and will) take its place instead.

                p {
                  height: 100px;
                  width: 100px;
                  display: none;
                }

visibility hidden : 

                If you only want to hide an element but you want to keep its place 
                (i.e. other elements don't fill the empty spot),you can use visibility: hidden.
                
                p {
                  height: 100px;
                  width: 100px;
                  visibility: hidden;
                }



#### inline-block : 

        two div can be brought in same line using inline-block, you can set width for div if you set display:inline-block.
        inline-block using in block elements like div, you can divide screen. but try to use flex.
