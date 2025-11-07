<script>
  import { NavigationBar } from 'statue-ssg';
  import { PageHero } from 'statue-ssg';
  import { Mission } from 'statue-ssg';
  import { Team } from 'statue-ssg';
  import { WhyChooseUs } from 'statue-ssg';
  import { CTA } from 'statue-ssg';
  
  export let data;
  
  $: directories = data.directories;
</script>

<svelte:head>
  <title>About Us | Statue SSG</title>
  <meta name="description" content="Learn about the team behind Statue SSG, our mission and values." />
</svelte:head>

<NavigationBar navbarItems={directories} activePath="/about" />

<div class="min-h-screen text-white bg-gradient-to-b from-[var(--color-hero-from)] via-[var(--color-hero-via)] to-[var(--color-hero-to)]">
  <!-- Hero Section -->
  <PageHero 
    title="About Statue SSG" 
    description="We're building the next generation of static site tools for creators and developers." 
  />

  <!-- Content Sections -->
  <div>
    <div class="container mx-auto px-4 py-16">
      <!-- Our Mission Section -->
      <Mission />
      
      <!-- Team Section -->
      <Team />
      
      <!-- Why Choose Us Section -->
      <WhyChooseUs />

      <!-- CTA Section -->
      <CTA />
    </div>
  </div>
</div>

<style>
  /* Page specific styles can go here */
</style> 