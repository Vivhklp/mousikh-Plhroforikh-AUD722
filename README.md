# mousikh-Plhroforikh-AUD722

s.boot; //

s.meter; //

/ *


* /

(~ mypiece = {arg freq = 9; var aud, vibrato;

vibrato = SinOsc.ar (freq, 0, 20, 300);
aud = SinOsc.ar (vibrato, mul: 0,6)! 2;
aud = aud + Pulse.ar (freq * [1, 1, 2,1], 0,1);    
aud = aud * Line.ar (1, 5, 8);    
aud = SinOsc.kr (1, mul: 50, add: 150);        
aud = SoundIn.ar ([0, 1]);

}; )

m = ~ mypiece.play [\ freq, 9]); //
m.set (\ gate, 9, \ fadeTime, 7); //
s.quit; //
