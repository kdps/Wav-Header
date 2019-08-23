8 bit mono

            ;---RIFF CHUNK-------------------------
db  'RIFF'  ;identifier
dd  ?       ;overall length=file length-8 (fill in)
db  'WAVE'  ;RIFF chunk type
            ;---FMT CHUNK--------------------------
db  'fmt '  ;identifier
dd  16      ;fmt chunk length
dw  1       ;type
            ;0=stereo
            ;1=mono
dw  1       ;number of channels
dd  ?       ;sample rate in hertz         (fill in)
dd  ?       ;bytes per second=sample rate (fill in)
dw  1       ;bytes per sample
            ;1= 8 bit mono
            ;2= 8 bit stereo or 16 bit mono
            ;4=16 bit stereo
dw  8       ;bits per sample (8,12,16)
            ;---DATA CHUNK-------------------------
db  'data'  ;identifier
dd  ?       ;data length=file length-44   (fill in)
            ;---DATA-------------------------------
