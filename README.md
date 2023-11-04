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

Norge
Sverige
Finland
Danmark
Faeroyene
Island


Oppgave 2

include shared-gdrive("dcic-2021","1wyQZj_L0qqV9Ekgr9au6RX2iqt2Ga8Ep")
include gdrive-sheets
include data-source
ssid = "1RYN0i4Zx_UETVuYacgaGfnFcv4l9zd9toQTTdkQkj7g"
consumer-data =
load-table: komponent, energi
source: load-spreadsheet(ssid).sheet-by-name("kWh", true)
   
    sanitize energi using string-sanitizer
end

fun energi-to-number(str :: String) -> Number:
  cases(Option) string-to-number(str):
    | some(a) => a
    | none => 0
  end
where: 
  energi-to-number("") is 0
  energi-to-number("48") is 48
  energi-to-number("37") is 37
end
