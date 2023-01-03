# Sarzn

input {
  display: grid;
  padding: 10px;
  filter: blur(4px) contrast(20) hue-rotate(53deg);
  background: #fff;
  mix-blend-mode: darken;
  -webkit-appearance: none;
  -moz-appearance: none;
  appearance: none;
}
input:before {
  content:"";
  width: 300px; /* control the size */
  aspect-ratio: 3;
  cursor: pointer;
  transition: .5s;
  background: linear-gradient(60deg,#f0f 49%,#0ff 51%) calc(100% - var(--p,0%))/240% 100%;
  --g:/calc(400%/15) 20% repeat-x linear-gradient(90deg,#000 75%,#0000 0);
  -webkit-mask:
    linear-gradient(#000 0 0) var(--p,calc(600%/7)) 75%/calc(100%/15) 20% no-repeat,
    0 0 var(--g),0 100% var(--g),0 50% var(--g),
    linear-gradient(90deg,#0000 50%,#000 0 75%,#0000 0) 0 25%/calc(400%/15) 20% repeat-x,
    linear-gradient(90deg,
      #000 calc(100%/15),#0000 0 calc(400%/15),#000 0 calc(500%/15),#0000 0 calc(600%/15),
      #000 0 calc(700%/15),#0000 0 calc(800%/15),#000 0 calc(900%/15),#0000 0) 
    0 75%/100% 20% no-repeat,
    repeating-conic-gradient(#0000 0 25%,#000 0 50%) 30.8% 32.5%/calc(40%/3) 40% no-repeat;
  -webkit-mask-composite: xor;
  mask-composite: exclude;
}
body:has(input:checked) {
  --p: 100%;
}
input:checked {
  --p: 100%;
}


body {
  min-height: 100vh;
  margin: 0;
  display: grid;
  place-content:center;
  background: linear-gradient(60deg,#e9e9c3 49%,#c6dfff 51%) var(--p,0%)/280% 100%;
  transition: .5s;
}

html {
  background: #fff;
}
