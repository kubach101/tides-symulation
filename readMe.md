##Wellcome to my project, I've made a simulation of a planet affected by tidal forces.##

######Physics foundation:######
At first I introduced my own units to avoid overflows. Then I added all the variables that matter.
Since my simulation features only a planet and much lighter satelite, I decided to ignore the slight movement of the planet becaose It would be unnoticeable.
<hr>

######Water modeling:######
I used the this function:
<img width="504" height="60" alt="image" src="https://github.com/user-attachments/assets/8267b351-7011-4f19-a476-b09e55ac931b" />


Taken from: https: //www.aanda.org/articles/aa/full_html/2012/08/aa19485-12/aa19485-12.html
But I only used the 2'nd term becaose rest is barely noticeable.
I am pretty interested so I learned how this function was made, I suggest you to see it yourelf becaose it uses few cool math tricks I didn't know were even useful.
<hr>

######Computing:######
The most computationally demanding was modeling the ocean. I managed to put it a shader, which worked perfectly becaose it required to go by every vertex.#
<hr>

####Graphics:####
I used GLFW and OpenGL(WebGL for web page)
For better visual representation I'va created scales that for eg. make the tides more visible
<hr>

####Website:####
After I modified my c code, I used emscripten, it can compile c code to WASM which is great for rendering e.t.c.
Emscripten: https://emscripten.org/
Then I added my own website features, for eg. sliders, touchpad.

