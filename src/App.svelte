<script lang="ts">
  import Icon from '@iconify/svelte';
  import { Box, ThemeIcon, SvelteUIProvider, TypographyProvider, ActionIcon, Text, Seo, Timeline, Paper } from '@svelteuidev/core';


  let isDark = false;

function toggleTheme() {
    isDark = !isDark;
}


</script>


<!-- set more here: https://www.svelteui.org/core/seo -->

<Seo
    title='Genetics Sim 3000'
    titleTemplate="%t%"
 />


  <SvelteUIProvider withNormalizeCSS withGlobalStyles themeObserver={isDark ? 'dark' : 'light'}>
    <TypographyProvider>
  



  
    
  



   <Box class="flex space-x-5 border-b h-16">

<Text class="mr-auto ml-5 my-auto text-2xl">Genetics simulator 3000</Text>

<ActionIcon class="mr-10 my-auto" on:click={toggleTheme} size="md" aria-label="Toggle theme">
 
  {#if isDark}
  <Icon icon="mdi:weather-sunny" />
{:else}
  <Icon icon="mdi:weather-night" />
{/if}

</ActionIcon>

   </Box>



<Box>

<Paper class="m-5">
 
   <Timeline active={1} bulletSize={24} lineWidth={2}>
   
    <Timeline.Item title='Generate genes'>
    	<svelte:fragment slot='bullet'>
			<ThemeIcon radius='xl' color='orange'><Icon color="white" icon="mdi:weather-sunny" /></ThemeIcon>
		</svelte:fragment>
		<Text color='dimmed' size='sm'>
			Generate 300 genes randomly, with a minimum of 130 each
		</Text>
    </Timeline.Item>
  
    <Timeline.Item title='Select 50'>
      <Text color='dimmed' size='sm'
        >Of the 300, select 50 at random<Text variant='link' root='span' href='#' inherit
          >fix-notifications branch</Text
        ></Text
      >
      <Text size='xs'>52 minutes ago</Text>
    </Timeline.Item>
  
    <Timeline.Item title='Pull request' lineVariant='dashed'>
      <Text color='dimmed' size='sm'
        >You&apos;ve submitted a pull request<Text variant='link' root='span' href='#' inherit
          >Fix incorrect notification message (#187)</Text
        ></Text
      >
      <Text size='xs'>34 minutes ago</Text>
    </Timeline.Item>
  
    <Timeline.Item title='Code review'>
      <Text color='dimmed' size='sm'
        ><Text variant='link' root='span' href='#' inherit>Robert Gluesticker</Text> left a code review on
        your pull request</Text
      >
      <Text size='xs'>12 minutes ago</Text>
    </Timeline.Item>

  </Timeline>

</Paper>

</Box>
  


 



</TypographyProvider>
</SvelteUIProvider>


