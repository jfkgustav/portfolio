<script lang="ts">
	import avatar from '$lib/assets/portfolio_bild.jpg';
  import linkedin from '$lib/assets/linkedin.png';
  import cv from '$lib/assets/cv.png';
  import * as Avatar from "$lib/components/ui/avatar";
  import cv_file from '$lib/assets/CV.pdf';
  import gitHub from "$lib/assets/Github.png";
  import epic from "$lib/assets/epic.png"
  import epic_square from "$lib/assets/epic_square.png"

  import { mediaQuery } from "svelte-legos";
  const isDesktop = mediaQuery("(min-width: 768px)");
</script>



<div class=" flex md:grid md:grid-cols-2 gap-40 text-center sm:text-left justify-center xl:py-20 h-full" style="background-image: url({epic}); background-repeat: no-repeat; background-size: cover;">


  <div class="sm:order-2 sm:hidden flex mx-auto drop-shadow-2xl z-0 relative justify-center">
    <img src={epic_square} alt="Find bild på mig :)" class="rounded-lg object-cover " />
  </div>

  <div class="container sm:w-full sm:px-10 sm:ml-32 my-auto rounded-lg p-5 z-20 absolute md:static mt-72 md:mt-0 w-full bg-slate-100 sm:bg-white">
    <h1 class="scroll-m-20 text-3xl font-extrabold tracking-tight lg:text-5xl">
      Gustav Johansson
    </h1>
    <h3 class="scroll-m-20 text-l tracking-tight lg:text-2xl text-gray-500">
      En kille som gillar sin dator
    </h3>

    <p class="scroll-m-20 text-md tracking-tight text-left lg:text-lg font-semibold py-5 text-gray-800">
      Jag har suttit vid datorn majoriteten av mitt liv och nu har jag även tänkt att det ska fortsätta så.
      Vid datorn gillar jag att skapa musik, programmera och så klart spela dataspel.  
    </p>


    <p class="hidden md:inline scroll-m-20 text-md tracking-tight lg:text-lg font-semibold text-gray-800">
      Klicka runt på sidan för att lära känna mig och 
      kika på lite grejor jag har hållit på med!
    </p>

    <p class="sm:hidden scroll-m-20 text-md tracking-tight lg:text-lg font-semibold text-gray-800">
      Klicka på hamburgaren!
    </p>

 

    <div class="grid grid-cols-2 sm:grid-cols-3 mt-5">

      <div class="container flex flex-col sm:flex-row items-center gap-x-3 p-0 "> 
        <a href={cv_file} download>
        <Avatar.Root>
          <Avatar.Image src={cv} alt="Mitt CV"/>
          <Avatar.Fallback>CV</Avatar.Fallback>
        </Avatar.Root>
        </a>
  
        <a href={cv_file} download class="scroll-m-20 text-l text-purple-600 tracking-tight lg:text-2xl">
          Hämta CV
        </a>
     </div>

      <div class="container flex flex-col sm:flex-row items-center gap-x-3 p-0 "> 
        <Avatar.Root >
          <a href="https://github.com/jfkgustav"><Avatar.Image src={gitHub} alt="github logo" /> </a>
          <Avatar.Fallback>GH</Avatar.Fallback>
        </Avatar.Root>

        <a href="https://github.com/jfkgustav" class="scroll-m-20 text-l text-[#0284c7] tracking-tight lg:text-2xl">
          Github
        </a>
      </div>



      <div class="hidden container flex flex-col sm:flex-row items-center gap-x-3 p-0 "> 
        <Avatar.Root>
          <Avatar.Image src={linkedin} alt="github logo" />
          <Avatar.Fallback>In</Avatar.Fallback>
        </Avatar.Root>

        <a href="https://github.com/jfkgustav" class="scroll-m-20 text-l text-[#0284c7] tracking-tight lg:text-2xl">
          Gustav Johansson
        </a>
      </div>

    </div>


  </div>




</div>

