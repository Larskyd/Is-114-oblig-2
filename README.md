# Is-114-oblig-2

Kode og funksjon for de nordiske flaggene

fun flagg(Top, Cross, Main): 
  frame( 
    overlay-xy(rectangle(220, 20, "solid", Cross),
      0, -70,
      overlay-xy(rectangle(20, 160, "solid", Cross),
        -70, 0,
        overlay-xy(square(60, "solid", Top),
          0, 0,
          overlay-xy(square(60, "solid", Top),
            0, -100,
            overlay-xy(rectangle(120, 60, "solid", Top),
              -100, -100,
              overlay-xy(rectangle(120, 60, "solid", Top),
                -100, 0,
                rectangle(220, 160, "solid", Main)))))))) 

  
end
Norge = flagg("red", "blue", "white")
Sverige = flagg("blue", "yellow", "yellow")
Finland = flagg("white", "blue", "blue")
Danmark = flagg("red", "white", "red")
Faeroyene = flagg("white", "red", "blue")
Island = flagg("blue", "red", "white")
