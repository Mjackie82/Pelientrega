<template>
  <section class="p-4 flex flex-col items-center">
    <div class="w-11/12">
      <h3 class="flex mb-2 font-thin text-lg self-start">Menu</h3>
      <div class="w-full flex justify-evenly">
        <button
          class="sm:w-40 p-2 flex gap-2 justify-center rounded-md items-center drop-shadow-md border bg-white border-white hover:border-blue-500"
        >
          <i class="fa-regular fa-square-plus"></i>Add Pedido
        </button>

        <button
          class="sm:w-40 p-2 flex gap-2 justify-center rounded-md items-center bg-white drop-shadow-md border border-white hover:border-blue-500"
        >
          <i class="fa-regular fa-file"></i>Baixar PDF
        </button>

        <button
          class="sm:w-40 p-2 flex gap-2 justify-center rounded-md items-center bg-white drop-shadow-md border border-white hover:border-blue-500"
        >
          <i class="fa-solid fa-filter"></i>Filtro
        </button>
      </div>
    </div>
    <div class="sm:w-11/12">
      <h3 class="flex mb-2 font-thin text-lg self-start">Pedidos</h3>
      <table class="w-full h-72 overflow-hidden drop-shadow-md">
        <thead>
          <tr class="font-semibold bg-yellow-400">
            <td class="p-4 rounded-tl-xl">#</td>
            <td>Pedido</td>
            <td>Entregador</td>
            <td>Horario</td>
            <td>entregue</td>
            <td class="text-center rounded-tr-xl">info</td>
          </tr>
        </thead>
        <tbody class="bg-white">
          <tr class="hover:bg-gray-100">
            <td class="p-1 border">1</td>
            <td class="p-1 border">pão</td>
            <td class="p-1 border">Felps</td>
            <td class="p-1 border">1 e ouco</td>
            <td class="p-1 border">sei lá</td>
            <td class="text-center border cursor-pointer">
              <i class="fa-solid fa-circle-info"></i>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
  </section>
</template>

<script setup></script>
