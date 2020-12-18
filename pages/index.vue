<template>
  <div>
    <HeroSection />
    <div class="container px-3 py-4 mx-auto flex flex-wrap flex-col justify-evenly md:flex-row items-center">
      <Card v-for="(item, index) in cardData" :key="index" :image="item.image" :title="item.title" :text="item.text">
      </Card>
    </div>
    <FAQs />
  </div>
</template>

<script>
import HeroSection from '~/components/Hero-Section';
import FAQs from '~/components/FAQs';
import Card from '~/components/Card';
export default {
  components: {Card, FAQs, HeroSection},
  data() {
    return {
      cardData: [
        {
          title: 'Our Team',
          image: 'https://secure.365forexreviews.com/pics/1603000235.png',
          text: 'We are a team of experts with over 10 years of trading experience. In this time, we\'ve reviewed over 200 brokers and have come across the good, the bad and the ugly.'
        },
        {
          title: 'Reviews',
          image: 'https://secure.365forexreviews.com/pics/1603000262.png',
          text: 'All of our reviews focus on over 200 criteria points. This includes considering trading platforms, bonuses, account types, fees and more.'
        },
        {
          title: 'Money and Time',
          image: 'https://secure.365forexreviews.com/pics/1603000294.png',
          text: 'We help you to save time, money and stress. Our experts spend several days carefully reviewing each broker we come across so that you don’t have to.'
        },
        {
          title: 'Best Brokers',
          image: 'https://secure.365forexreviews.com/pics/1603000262.png',
          text: 'We help traders to not only find great brokers but to progress in their trading career.'
        }
      ]
    };
  }
}
</script>

<style>
/* Sample `apply` at-rules with Tailwind CSS
.container {
@apply min-h-screen flex justify-center items-center text-center mx-auto;
}
 */
</style>
