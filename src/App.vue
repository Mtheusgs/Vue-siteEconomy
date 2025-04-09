<script setup lang="ts">

  import { onMounted, reactive,ref } from 'vue'; // Importa as funções necessárias

  // Criação da variável reativa para a mensagem
  const mensagem = reactive({
    nome: "Eduarda Rabelo",
    mostrarMensagem: true,
  }); 

  const Saldo = ref(400)

  // Hook onMounted para esconder a mensagem após 5 segundos
  onMounted(() => {
    setTimeout(() => {
      mensagem.mostrarMensagem = false;
    }, 5000);
  }); 

  

  
  
</script>

<template>
  <body class="bg-gray-200 min-h-screen w-full flex flex-row gap-4">
    <!-- naBar -->
    <div class="w-[4%] border-r-1 border-gray-300 flex flex-col items-center justify-between pt-5 pb-7">
      <!-- Bolinha amarela no topo -->
      <div class="w-10 h-10 rounded-full bg-yellow-400 mt-4 flex items-center justify-center"> 
        <svg xmlns="http://www.w3.org/2000/svg" width="2em" height="2em" viewBox="0 0 32 32"><!-- Icon from Fluent Emoji High Contrast by Microsoft Corporation - https://github.com/microsoft/fluentui-emoji/blob/main/LICENSE --><path fill="#000000" d="M23.07 2c-.57-.01-1.13.061-1.66.18a.98.98 0 0 0-.595 1.51q.004.004.005.011c.23.35.65.52 1.06.43c.36-.09.74-.13 1.12-.13c2.84 0 5.14 2.38 4.99 5.25a5 5 0 0 1-1.385 3.2l.04.076a6.49 6.49 0 0 0-5.145-2.526c-.98 0-1.96.22-2.84.65l-4.77 2.32c-.41.2-.88-.1-.88-.55v-1.33c0-1.25-.47-2.39-1.24-3.26l-4.05-4.51c-.25-.28-.72-.11-.72.27v2.71c-1.87.43-3.34 2.32-3.72 4.27c-.05.25-.27.43-.52.43a.76.76 0 0 0-.76.76v.22c0 2.22 1.8 4.02 4.02 4.02v1.59a4.41 4.41 0 0 0 3.98 4.39v6.65c0 .2.17.37.38.37h2.25c.21 0 .38-.17.38-.38v-5.879l1.4 5.879c.06.22.26.38.49.38h2.13c.24 0 .42-.23.36-.45l-1.557-6.55h4.014l-1.557 6.55c-.06.22.12.45.36.45h2.13c.23 0 .43-.16.49-.38l1.17-4.91l.95.95c.21.21.27.52.15.79l-1.3 3.03c-.12.24.06.52.33.52h2.18c.15 0 .29-.09.34-.23l2.52-5.89c.26-.58.39-1.21.39-1.84v-4.54c0-.784-.139-1.535-.393-2.231A7 7 0 0 0 30 8.9c-.05-3.78-3.15-6.86-6.93-6.9M5.813 10.747c0-.359.29-.637.637-.637c.359 0 .637.29.637.637v.95a.64.64 0 0 1-.637.637a.635.635 0 0 1-.637-.637z"></path></svg>
      </div>

      <!-- Ícones -->
      <div class="flex flex-col items-center gap-10"> 
        <svg class="border-b-1 border-gray-300 cursor-pointer bg-gray-200 rounded-sm hover:bg-gray-300 hover:text-transparent  p-1" xmlns="http://www.w3.org/2000/svg" width="2.2em" height="2.2em" viewBox="0 0 24 24"><g fill="none" stroke="#888888" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" color="currentColor"><path d="m9 22l.002-4.002c0-.931 0-1.396.153-1.763a2 2 0 0 1 1.083-1.083C10.605 15 11.07 15 12 15v0c.93 0 1.396 0 1.764.152a2 2 0 0 1 1.083 1.083C15 16.603 15 17.068 15 18v4"></path><path d="m7.088 4.762l-1 .781c-1.516 1.184-2.275 1.776-2.681 2.61C3 8.988 3 9.952 3 11.88v2.092c0 3.784 0 5.676 1.172 6.852S7.229 22 11 22h2c3.771 0 5.657 0 6.828-1.176S21 17.756 21 13.971v-2.09c0-1.929 0-2.893-.407-3.728c-.407-.834-1.165-1.426-2.681-2.61l-1-.78C14.552 2.92 13.372 2 12 2s-2.552.92-4.912 2.762"></path></g></svg>
        <svg class="border-b-1 border-gray-300 cursor-pointer bg-gray-200 rounded-sm hover:bg-gray-300 hover:text-transparent  p-1" xmlns="http://www.w3.org/2000/svg" width="2.2em" height="2.2em" viewBox="0 0 36 36"><circle cx="13.33" cy="29.75" r="2.25" fill="#888888" class="clr-i-outline clr-i-outline-path-1"></circle><circle cx="27" cy="29.75" r="2.25" fill="#888888" class="clr-i-outline clr-i-outline-path-2"></circle><path fill="#888888" d="M33.08 5.37a1 1 0 0 0-.77-.37H11.49l.65 2H31l-2.67 12h-15L8.76 4.53a1 1 0 0 0-.66-.65L4 2.62a1 1 0 1 0-.59 1.92L7 5.64l4.59 14.5l-1.64 1.34l-.13.13A2.66 2.66 0 0 0 9.74 25A2.75 2.75 0 0 0 12 26h16.69a1 1 0 0 0 0-2H11.84a.67.67 0 0 1-.56-1l2.41-2h15.44a1 1 0 0 0 1-.78l3.17-14a1 1 0 0 0-.22-.85" class="clr-i-outline clr-i-outline-path-3"></path><path fill="none" d="M0 0h36v36H0z"></path></svg>
        <svg class="border-b-1 border-gray-300 cursor-pointer bg-gray-200 rounded-sm hover:bg-gray-300 hover:text-transparent p-1" xmlns="http://www.w3.org/2000/svg" width="2.2em" height="2.2em" viewBox="0 0 32 32">><path fill="#888888" d="M16 2a9 9 0 0 0-6 15.69V30l6-4l6 4V17.69A9 9 0 0 0 16 2m4 24.26l-2.89-1.92L16 23.6l-1.11.74L12 26.26v-7.21a8.88 8.88 0 0 0 8 0ZM20.89 16A7 7 0 1 1 23 11a7 7 0 0 1-2.11 5"></path></svg>
        <svg class="border-b-1 border-gray-300 cursor-pointer bg-gray-200 rounded-sm hover:bg-gray-300 hover:text-transparent  p-1" xmlns="http://www.w3.org/2000/svg" width="2.2em" height="2.2em" viewBox="0 0 32 32"><g fill="#888888"><path d="M9.117 14.64a.377.377 0 0 1 .533.007l.511.524c.569-.427 1.13-.461 1.578-.345a2 2 0 0 1 .799.42l.014.013l.005.005l.002.001v.001l-.257.272l.258-.272a.378.378 0 0 1-.518.55l-.004-.004l-.022-.018a1.3 1.3 0 0 0-.467-.237c-.274-.072-.675-.067-1.142.4s-.468.862-.396 1.128a1.2 1.2 0 0 0 .255.477a1 1 0 0 0 .109.08c.083.055.2.116.34.15c.255.062.645.054 1.118-.419c.326-.326.665-.512 1-.591c.335-.08.642-.047.896.027a2.15 2.15 0 0 1 .812.45l.014.013l.005.004l.002.002s.001.001-.262.272l.29-.24h.002l.002.003l.003.005l.012.014a1.5 1.5 0 0 1 .133.207c.074.135.16.33.206.568c.08.42.025.944-.37 1.47l.59.598a.377.377 0 1 1-.536.53l-.586-.592c-.532.4-1.061.453-1.486.37a2 2 0 0 1-.778-.344l-.015-.012l-.005-.004l-.002-.001v-.001l.24-.291l-.24.291a.378.378 0 0 1 .479-.583l.002.002l.02.015q.031.022.095.058c.085.048.206.101.35.13c.264.051.65.027 1.087-.41c.438-.438.464-.823.414-1.085a1.2 1.2 0 0 0-.183-.437l-.003-.005l-.01-.009a1.4 1.4 0 0 0-.492-.264a1 1 0 0 0-.511-.016c-.183.043-.402.15-.641.39c-.657.657-1.317.744-1.83.618a1.9 1.9 0 0 1-.778-.403l-.014-.013l-.004-.005l-.002-.002h-.001L10 17.83l-.27.264v-.001l-.003-.002l-.004-.005l-.013-.014l-.04-.046a2 2 0 0 1-.388-.744c-.12-.447-.087-1.008.345-1.578l-.517-.53a.377.377 0 0 1 .007-.534"></path><path d="m10 17.83l-.262.272l-.008-.008zm4.3-.28l.262-.271l.016.015l.013.016z"></path><path d="m11.354 25.958l-.011-.01l-7.49-7.49a2.75 2.75 0 0 1 0-3.885l4.17-4.163H6.64a1.856 1.856 0 0 1-1.857-1.76a2 2 0 0 1 .427.049H8.9v-.344H5.21a1.856 1.856 0 0 1-1.817-1.46q.215.053.447.054h4.627v-.344H4.174c-1.064 0-1.945-.651-2.132-1.516h8.968a2.67 2.67 0 0 1 1.717.622l3.916-3.91a2.75 2.75 0 0 1 3.884 0l1.868 1.872q.038.033.072.069l7.49 7.49c1.064 1.064 1.057 2.807-.01 3.874l-4.784 4.785c.17.353.267.75.267 1.168v8.968c-.865-.187-1.516-1.068-1.516-2.132V23.75h-.344v4.627q0 .15.023.293a1.86 1.86 0 0 1-1.43-1.81v-3.69h-.343v3.69q0 .221.049.427c-.985-.052-1.795-.86-1.795-1.857v-.45l-2.907 2.907a2.75 2.75 0 0 1-3.884 0l-1.926-1.926zm6.703-22.74l-4.373 4.366a2.7 2.7 0 0 1-.028.616l1.824 1.824a3.412 3.412 0 0 1 6.65 1.066a3.41 3.41 0 0 1-2.344 3.24l2.115 2.115l4.692-4.692a.74.74 0 0 0 0-1.046l-7.48-7.49a.75.75 0 0 0-1.056 0m-7.817 7.804l-4.973 4.965a.75.75 0 0 0 0 1.056l7.49 7.49a.75.75 0 0 0 1.056 0l4.97-4.97z"></path></g></svg>
      </div>

      <!-- Espaço vazio para o "final" -->
      <div class="w-10 h-10 rounded-full bg-yellow-400 mt-4 flex items-center justify-center overflow-hidden cursor-pointer">
        <svg xmlns="http://www.w3.org/2000/svg" width="3em" height="3em" viewBox="0 0 512 512">
          <path fill="#000000" d="m448 362.7l-117.3-21.3C320 320 320 310.7 320 298.7c10.7-10.7 32-21.3 32-32c10.7-32 10.7-53.3 10.7-53.3c5.5-8 21.3-21.3 21.3-42.7s-21.3-42.7-21.3-53.3C362.7 32 319.2 0 256 0c-60.5 0-106.7 32-106.7 117.3c0 10.7-21.3 32-21.3 53.3s15.2 35.4 21.3 42.7c0 0 0 21.3 10.7 53.3c0 10.7 21.3 21.3 32 32c0 10.7 0 21.3-10.7 42.7L64 362.7C21.3 373.3 0 448 0 512h512c0-64-21.3-138.7-64-149.3"></path>
        </svg>
      </div>
    </div>

    <div class="w-[96%] flex flex-col p-6"> 

      <div class="flex flex-row items-center justify-between h-[80px] mt-6 "> 

        <div class="flex flex-row p-4 gap-4 items-center justify-center">

          <h4 class="font-bold text-lg w-25 h-6 border-r-1 border-gray-300 ">Black Cat</h4> 
          <div class="flex flex-row gap-4 items-center justify-center">  
            <svg xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 16 16"><path fill="#888888" d="m11.271 11.978l3.872 3.873a.5.5 0 0 0 .708 0a.5.5 0 0 0 0-.708l-3.565-3.564c2.38-2.747 2.267-6.923-.342-9.532c-2.73-2.73-7.17-2.73-9.898 0s-2.728 7.17 0 9.9a6.96 6.96 0 0 0 4.949 2.05a.5.5 0 0 0 0-1a5.96 5.96 0 0 1-4.242-1.757a6.01 6.01 0 0 1 0-8.486a6.004 6.004 0 0 1 8.484 0a6.01 6.01 0 0 1 0 8.486a.5.5 0 0 0 .034.738"></path></svg>
            <p class=" text-lg w-25 h-6 text-gray-400">Search</p>
          </div>

        </div>  

        <div class="flex flex-row items-center gap-6">

          <svg class="cursor-pointer" xmlns="http://www.w3.org/2000/svg" width="1.5em" height="1.5em" viewBox="0 0 24 24"><path fill="#fbbf24" d="M3 6v14a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2V6a2 2 0 0 0-2-2h-2V2h-2v2H9V2H7v2H5a2 2 0 0 0-2 2m16 14H5V8h14z"></path></svg> 

          <div class="flex flex-row p-4 gap-4 border-2 rounded-2xl  h-8 items-center font-bold"> 
          
          <h3 class=" " v-show="mensagem.mostrarMensagem">Seja bem vinda, {{ mensagem.nome }}!</h3>   <!-- v-show = verifica e está sempre no código html (independente do resultado, trabalha com display) -->
          <div class="flex flex-row gap-2 items-center justify-center " v-show="!mensagem.mostrarMensagem">
            <svg xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 26 26"><path fill="currentColor" d="M16.563 15.9c-.159-.052-1.164-.505-.536-2.414h-.009c1.637-1.686 2.888-4.399 2.888-7.07c0-4.107-2.731-6.26-5.905-6.26c-3.176 0-5.892 2.152-5.892 6.26c0 2.682 1.244 5.406 2.891 7.088c.642 1.684-.506 2.309-.746 2.397c-3.324 1.202-7.224 3.393-7.224 5.556v.811c0 2.947 5.714 3.617 11.002 3.617c5.296 0 10.938-.67 10.938-3.617v-.811c0-2.228-3.919-4.402-7.407-5.557"></path></svg>
            <h3 class=" border-gray-400"  v-show="!mensagem.mostrarMensagem">{{ mensagem.nome }}</h3>
          </div> 

        </div>
        </div>



      </div> 

      <div class="w-full h-[500px] flex flex-row p-6 gap-4"> 


        <div class="w-3/4 bg-white h-[400px] rounded-lg  p-4 gap-4 flex flex-col">  
          
          <h1 class="font-light text-6xl">Per Week</h1>

          <div class="w-full h-full grid grid-cols-6 grid-rows-6 gap-4">
            <div class="col-span-2 row-span-3 bg-yellow-400 rounded-2xl p-4 flex flex-row-reverse items-end text-3xl" >
              ${{ Saldo }}
            </div> 

            <div class="col-span-2 row-span-3 bg-gray-400 rounded-2xl" ></div>

            <div class="col-span-2 row-span-3 bg-black rounded-2xl" ></div>
          </div>

          

        </div>  

        <div class="w-1/4 bg-white h-[700px] rounded-lg grid grid-rows-4 p-10">
          <div class="row-span-1 bg-gray-300 rounded-2xl" ></div>
        </div> 


      </div>

      

    </div>

  </body>
</template>


<style scoped>

</style>
