# Sound not working

I fixed this by following [this video](https://www.youtube.com/watch?v=oWF3l4O7AeI). Thanks! :cake:

 1. Install the needed tools
 
   ```sh
   sudo apt-get install alsa-utils mpg321 lame
   ```

 2. Load the sound driver
 
   ```sh
  sudo modprobe snd bcm2835
   ```
   
 3. *Optionally*, check if it's working:
 
  ```sh
  sudo lsmod | grep 2835
  ```
  
 4. Then run (honestly, I don't know what kind of black magic is this–[explainations are welcome](/CONTRIBUTING.md)!):
 
  ```sh
  sudo amixer cset numid=3 1
  ```

Then, to test if everything worked, I did `espeak -ven 'Hi there!'`–you are supposed to hear in the headphones/speakers *Hi there*. If you don't have `espeak` installed, do `sudo apt-get install espeak` to install it.
