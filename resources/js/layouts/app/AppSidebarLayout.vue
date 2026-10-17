<script setup lang="ts">
import AppContent from '@/components/AppContent.vue';
import AppShell from '@/components/AppShell.vue';
import { Toaster } from '@/components/ui/sonner';
import type { BreadcrumbItem } from '@/types';

type Props = {
    breadcrumbs?: BreadcrumbItem[];
};

withDefaults(defineProps<Props>(), {
    breadcrumbs: () => [],
});
</script>

<template>
    <AppShell variant="sidebar">
        <!-- <AppSidebar /> -->
        
            <!-- <AppSidebarHeader :breadcrumbs="breadcrumbs" /> -->
            <slot />
       
        <Toaster />
    </AppShell>
</template>
