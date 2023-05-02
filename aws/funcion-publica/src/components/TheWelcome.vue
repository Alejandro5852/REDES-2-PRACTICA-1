<script setup>
import WelcomeItem from './WelcomeItem.vue'
import DocumentationIcon from './icons/IconDocumentation.vue'
import ToolingIcon from './icons/IconTooling.vue'
import EcosystemIcon from './icons/IconEcosystem.vue'
import CommunityIcon from './icons/IconCommunity.vue'
import SupportIcon from './icons/IconSupport.vue'
</script>

<template>
    <WelcomeItem>
    <template #icon>
      <DocumentationIcon />
    </template>
    <template #heading>Desarrolladores</template>

    <ul>
      <li>César Alejandro Sosa Enríquez - 201800555</li>
      <li>Ricardo Enrique Fernandez De La Roca - 200611606</li>
      <li>Keila Avril Vilchez Suarez - 201700569</li>
    </ul>
  </WelcomeItem>




  <WelcomeItem>
    <template #icon>
      <CommunityIcon />
    </template>
    <template #heading>Administradores</template>
    <ul>
      <li>Eddie Orlando Xuyá Monroy - 201113930</li>
      <li>Wilson Eduardo Perez Echeverria - 201709110</li>
    </ul>
  </WelcomeItem>


</template>
