# FaustWebAudioInput
A repo to show how to get an audio track hooked up into the input of a faust patch. 

Look at audioinput.dsp, the audio is being fed into the patch to begin with by using the 'plus/ add' operator: '+'. NB the example is a mono input being fed to stereo. 

If you'd to replicate the faust patch is exported using the instructions: 

faust2wasm -worklet audioinput.dsp

I followed along with this instructions to get an audio file playing: 

https://developer.mozilla.org/en-US/docs/Web/API/Web_Audio_API/Using_Web_Audio_API

To hook the audio file up into the faust graph, have a look at the startaudioinput function, startiing line 87: of the .html file, ln: 97 is where the audio track is connected to the graph via track.connect(faust_dsp)
