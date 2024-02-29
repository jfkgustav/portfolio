<script lang="ts">
  import * as Carousel from "$lib/components/ui/carousel/index.js";
  import jointfly_start from '$lib/assets/jointfly_start.png';
  import jointfly_play from '$lib/assets/jointfly_play.png';
  import recharge from '$lib/assets/recharge.png';
  import three_d_studio_one from '$lib/assets/3d_studio_one.png';
  import three_d_parallel from '$lib/assets/3d_parallel.png';
  import three_d_oblique from '$lib/assets/3d_oblique.png';
  import skrivert_meme from '$lib/assets/skrivert_meme.jpg';
</script>

<div class="container pb-20" id="grafikmotor">
  <h1 class="text-center text-4xl font-extrabold tracking-tight lg:text-3xl">
    3D Studio
  </h1>
  

  <h3 class="text-md text-center font-semibold leading-none py-3">
    Simpel grafikmotor skriven i C++ med hjälp av OpenGL, GLM och tinyOBJloader
  </h3>

  <div class="container ">
    <Carousel.Root
      opts={{
        align: "start",
        loop: true,
      }}
    >
      
      <Carousel.Content class="mx-auto">
        <Carousel.Item>
          <img src={three_d_studio_one} alt="3D studio bild 1" class="mx-auto w-1/2"/>
          <p class="text-md text-center text-xl font-semibold leading-none py-3"> 3D Studio </p>
        </Carousel.Item>
        <Carousel.Item>
          <img src={three_d_parallel} alt="Parallel Projektion" class="mx-auto w-1/2"/>
          <p class="text-md text-center font-semibold leading-none py-3"> Parallel Projection </p>
        </Carousel.Item>
        <Carousel.Item>
          <img src={three_d_oblique} alt="Oblik Projektion" class="mx-auto w-1/2"/>
          <p class="text-md text-center font-semibold leading-none py-3"> Oblique Projection </p>
        </Carousel.Item>
      </Carousel.Content>
      <Carousel.Previous/>
      <Carousel.Next/>
    </Carousel.Root>
  </div>
</div>


 

<div class="container pb-20" id="recharge">
  <h1 class="text-center text-4xl font-extrabold tracking-tight lg:text-3xl">
    RECHARGE
  </h1>
  

  <h3 class="text-md text-center font-semibold leading-none py-3">
    En app för att smidigt hitta och boka laddstationer för elbilar
  </h3>


  <img src={recharge} alt="recharge" class="mx-auto w-1/2"/>
  <p class="text-md text-center font-semibold leading-none py-3"> RECHARGE </p>

</div>


 

<div class="container pb-20" id="jointfly">
  <h1 class="text-center text-4xl font-extrabold tracking-tight lg:text-3xl">
    jointfly!
  </h1>
  

  <h3 class="text-md text-center font-semibold leading-none py-3">
    En app för att styra flera drönare samtidigt från en mobil enhet.
  </h3>


  <Carousel.Root
    opts={{
      align: "start",
      loop: true,
    }}
  >
    
    <Carousel.Content class="mx-auto">
      <Carousel.Item>
        <img src={jointfly_start} alt="jointfly startskärm" class="mx-auto w-1/2"/>
        <p class="text-md text-center font-semibold leading-none py-3"> jointflys startskärm </p>
      </Carousel.Item>
      <Carousel.Item>
        <img src={jointfly_play} alt="jointfly körs" class="mx-auto w-1/2"/>
        <p class="text-md text-center font-semibold leading-none py-3"> Bild på när jointfly körs </p>
      </Carousel.Item>
    </Carousel.Content>
    <Carousel.Previous class=""/>
    <Carousel.Next />
  </Carousel.Root>
</div>


<div class="container pb-20" id="skrivert">
  <h1 class="text-center text-4xl font-extrabold tracking-tight lg:text-3xl">
    skrivert
  </h1>
  

  <h3 class="text-md text-center font-semibold leading-none py-3">
    Projekt för att skapa GUI till en textproduktionsapplikation
  </h3>


  <img src={skrivert_meme} alt="skrivert meme if i had any" class="mx-auto h-[400px]"/>
  <p class="text-md text-center font-semibold leading-none py-3"> Än så länge har vi inte kommit så långt i detta projekt :) </p>

  
</div>

