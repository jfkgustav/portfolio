<script lang="ts">
	import avatar from '$lib/assets/portfolio_bild.jpg';
  import linkedin from '$lib/assets/linkedin.png';
  import cv from '$lib/assets/cv.png';
  import * as Avatar from "$lib/components/ui/avatar";
  import cv_file from '$lib/assets/CV.pdf';
  import gitHub from "$lib/assets/Github.png";
</script>



<div class="container md:grid md:grid-cols-2 gap-40 justify-center xl:py-32">

  <div class="my-auto rounded-lg p-5">
    <h1 class="scroll-m-20 text-3xl font-extrabold tracking-tight lg:text-5xl">
      Gustav Johansson
    </h1>
    <h3 class="scroll-m-20 text-l tracking-tight lg:text-2xl text-gray-500">
      En kille som gillar sin dator
    </h3>

    <p class="scroll-m-20 text-md tracking-tight lg:text-lg font-semibold py-10 text-gray-800">
      Jag har suttit vid datorn majoriteten av mitt liv och nu har jag även tänkt att det ska fortsätta så.
      Vid datorn gillar jag att skapa musik, programmera och så klart spela dataspel. <br> <br> Klicka runt på sidan för att lära känna mig och 
      kika på lite grejor jag har hållit på med!
    </p>

    <div class="grid grid-cols-3">
    <div class="container flex items-center gap-x-3 p-0 "> 
      <Avatar.Root>
        <Avatar.Image src={gitHub} alt="github logo" />
        <Avatar.Fallback>In</Avatar.Fallback>
      </Avatar.Root>

      <a href="https://github.com/jfkgustav" class="scroll-m-20 text-l text-[#0284c7] tracking-tight lg:text-2xl">
        jfkgustav
      </a>
    </div>

    <div class="container flex items-center gap-x-3 p-0 "> 
        <Avatar.Root>
          <Avatar.Image src={cv} alt="Mitt CV" />
          <Avatar.Fallback>CV</Avatar.Fallback>
        </Avatar.Root>
  
        <a href={cv_file} download class="scroll-m-20 text-l text-purple-600 tracking-tight lg:text-2xl">
          Hämta CV
        </a>
    </div>
  </div>


  </div>




  <div class="mx-auto drop-shadow-2xl">
      <img src={avatar} alt="Find bild på mig :)" class="border border-orange-500 aspect-square w-[500px] rounded-full object-cover object-right-top " />
  </div>

</div>

