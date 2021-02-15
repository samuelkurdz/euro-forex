<template>
  <section>
    <div class="pt-24">
      <div class="container px-3 mx-auto flex flex-wrap flex-col md:flex-row items-center">
        <!--Left Col-->
        <div class="flex flex-col w-full md:w-2/5 justify-center items-start text-center md:text-left">
          <p class="uppercase tracking-loose w-full">Forex Brokers Trading</p>
          <h1 class="my-4 text-5xl font-bold leading-tight">
            Forex Brokers Trading
          </h1>
          <p class="leading-normal text-xl mb-8">
            The forex market is the largest and most liquid financial market in the world,
            where currencies are traded against each other in currency pairs by individuals,
            known as retail traders, banks and large corporations.

          </p>
          <button class="inline-block px-6 py-2 m-auto text-xs font-medium leading-6 text-center text-white uppercase transition
                         bg-gray-800 rounded shadow ripple waves-light hover:shadow-lg focus:outline-none hover:bg-black">
            Subscribe
          </button>
        </div>
        <!--Right Col-->
        <div class="w-full md:w-3/5 py-6 text-center">
          <img class="w-full md:w-4/5 z-50" src="/hero-banner.png"  alt="hero-image"/>
        </div>
      </div>
    </div>
    <div
      style="height:fit-content; overflow: hidden; font-size: 12px; padding:1px; width: 100%;">
      <div style="height:40px; width: 100%;">
        <iframe src="https://widget.coinlib.io/widget?type=horizontal_v2&theme=light&pref_coin_id=1505&invert_hover=" width="100%" height="36px" scrolling="auto" marginwidth="0" marginheight="0" frameborder="0" border="0" style="border:0;margin:0;padding:0;">
        </iframe>
      </div>
    </div>

    <div class="flex flex-row mt-2 justify-between p-4">
      <div style="height:560px; background-color: #FFFFFF; overflow:hidden; box-sizing: border-box; border: 1px solid #56667F;
                border-radius: 4px; text-align: right; line-height:14px; font-size: 12px; font-feature-settings: normal; text-size-adjust: 100%;
                box-shadow: inset 0 -20px 0 0 #56667F;padding:1px;padding: 0px; margin: 0px; width: 80%;">
        <div style="height:540px; padding:0px; margin:0px; width: 100%;">
          <iframe src="https://widget.coinlib.io/widget?type=chart&theme=light&coin_id=859&pref_coin_id=1505" width="100%" height="536px" scrolling="auto" marginwidth="0" marginheight="0" frameborder="0" border="0" style="border:0;margin:0;padding:0;line-height:14px;">
          </iframe>
        </div>
      </div>
      <div style="width: 250px; height:335px; background-color: #FAFAFA; overflow:hidden; box-sizing: border-box; border: 1px solid #56667F;
    border-radius: 4px; text-align: right; line-height:14px; block-size:335px; font-size: 12px; font-feature-settings: normal; text-size-adjust: 100%;
    box-shadow: inset 0 -20px 0 0 #56667F;margin: 0;width: 250px;padding:1px;padding: 0px; margin: 0px;"
      >
        <div style="height:315px; padding:0px; margin:0px; width: 100%;">
          <iframe src="https://widget.coinlib.io/widget?type=converter&theme=light" width="250" height="310px" scrolling="auto" marginwidth="0" marginheight="0" frameborder="0" border="0" style="border:0;margin:0;padding:0;">
          </iframe>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
name: "Hero-Section"
}
</script>

<style scoped>

</style>
