###Documentation

setcps 1

d1 $ palindrome $ sound "bd*4 bd"
 
d2 $ sound "sn ~ sn ~"

d3 $ sound "hh*8"
 
d4 $ palindrome $ n (scale "minor" "0 2 4 5 7 9 6 11") 
  # s "arpy"
  # gain 0.7
  # pan (range 0.3 0.7 $ slow 4 sine) -- Apply panning with a sine wave LFO
  # room "0.6"
  # sz "0.5" -- Set the size of the room reverb

