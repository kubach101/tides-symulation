# TIDAL SIMULATION BY KUBA CHMURA

## Wellcome to my project, I've made a simulation of a planet affected by tidal forces

### Physics foundation

At first I introduced my own units to avoid overflows. Then I added all the variables that matter.
Since my simulation features only a planet and much lighter satelite, I decided to ignore the slight movement of the planet becaose It would be unnoticeable.

### Water modeling

The whole idea is if you know that for every particle the potencial on the surface must be constant you can approximate the shape when you also know that the water's volume can't change.
Learned from this article: <https://www.aanda.org/articles/aa/full_html/2012/08/aa19485-12/aa19485-12.html>
But I only used the 2'nd term becaose rest is barely noticeable.
I am pretty interested so I learned how this function was made, I suggest you to see it yourelf becaose it uses few cool math tricks I didn't know were even useful.

### Computing

The most computationally demanding was modeling the ocean. I managed to put it a shader, which worked perfectly becaose it required to go by every vertex.

### Graphics

I used GLFW and OpenGL(WebGL for web page).
For better visual representation I've created scales that for eg. make the tides more visible.
I wrote my own shaders, they aren't seperate files, becaose I wanted to have them as c-strings already in main.c

### Website

After I modified my c code, I used emscripten, it can compile c code to WASM which is great for rendering e.t.c.
Emscripten: <https://emscripten.org/>
Then I added my own website features, for eg. sliders, touchpad.
