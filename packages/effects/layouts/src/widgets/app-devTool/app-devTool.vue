<script lang="ts" setup>
import { BookOpenText } from '@vben/icons';
// import { SquareArrowDownLeft, SquareArrowUpRight } from '@vben/icons';

import { VbenIconButton } from '@vben-core/shadcn-ui';

function handleAppDevTool() {
  window.ipcRenderer?.invoke('app-devTool');
}
</script>
<template>
  <div class="flex-center mr-2 h-full" @click.stop="handleAppDevTool()">
    <VbenIconButton class="bell-button text-foreground relative">
      <BookOpenText class="size-4" />
    </VbenIconButton>
  </div>
</template>
