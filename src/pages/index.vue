<script setup lang="ts">
import { Button } from '@/components/ui/button'
import {
  Card,
  CardContent,
  CardFooter,
  CardHeader,
  CardTitle,
} from '@/components/ui/card'
</script>

<template>
  <div class="min-h-screen flex items-center justify-center bg-background text-foreground p-6">
    <div class="max-w-2xl w-full space-y-6">
      <h1 class="text-3xl font-semibold">
        shadcn-vue + Tailwind Integration Test
      </h1>
      <p class="text-sm text-muted-foreground">
        This page verifies Tailwind is loaded and theme variables apply. The
        styled button and card below should reflect Tailwind/shadcn theme tokens.
      </p>

      <div class="flex items-center gap-4">
        <Button>Primary Button</Button>
        <Button variant="outline">
          Secondary
        </Button>
      </div>

      <Card>
        <CardHeader>
          <CardTitle>Card</CardTitle>
        </CardHeader>
        <CardContent>
          <p class="text-sm text-muted-foreground">
            If this card background and text colors look correct, theme variables
            and Tailwind layers are working.
          </p>
        </CardContent>
        <CardFooter>
          <Button variant="ghost">
            Action
          </Button>
        </CardFooter>
      </Card>

      <div class="mt-4">
        <p class="text-xs text-muted-foreground">
          shadcn-vue components scaffolded — buttons and card above are
          from the library.
        </p>
      </div>
    </div>
  </div>
</template>

<style scoped></style>
