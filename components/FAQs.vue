<template>
  <section class="FAQs">
    <div class="w-full md:w-3/5 mx-auto p-8">
      <p class="m-auto"><strong>Frequently Asked Questions</strong></p>
      <div class="shadow-md">
        <div class="tab w-full overflow-hidden border-t">
          <input class="absolute opacity-0" id="tab-single-one" type="radio" name="tabs2">
          <label class="block p-5 leading-normal cursor-pointer" for="tab-single-one">
            Are CySEC, FSCA, FCA, AFM and ASIC regulated brokers safe for trading?
          </label>
          <div class="tab-content overflow-hidden border-l-2 bg-gray-100 border-indigo-500 leading-normal">
            <p class="p-5">
              These regulatory bodies ensures that their licences are not abused so therefore,
              they monitor events from how brokers interact with their client and they are always there to ensure client's safety.
            </p>
          </div>
        </div>
        <div class="tab w-full overflow-hidden border-t">
          <input class="absolute opacity-0" id="tab-single-two" type="radio" name="tabs2">
          <label class="block p-5 leading-normal cursor-pointer" for="tab-single-two">
            What would be the best broker for a forex beginner?
          </label>
          <div class="tab-content overflow-hidden border-l-2 bg-gray-100 border-indigo-500 leading-normal">
            <p class="p-5">
              Here are few of the brokers which have proven to ensure beginners get the most viable education which is a roadmap to successful trader.
            </p>
          </div>
        </div>
<!--        <div class="tab w-full overflow-hidden border-t">-->
<!--          <input class="absolute opacity-0" id="tab-single-three" type="radio" name="tabs2">-->
<!--          <label class="block p-5 leading-normal cursor-pointer" for="tab-single-three">Label Three</label>-->
<!--          <div class="tab-content overflow-hidden border-l-2 bg-gray-100 border-indigo-500 leading-normal">-->
<!--            <p class="p-5">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Tenetur, architecto, explicabo perferendis nostrum, maxime impedit atque odit sunt pariatur illo obcaecati soluta molestias iure facere dolorum adipisci eum? Saepe, itaque.</p>-->
<!--          </div>-->
<!--        </div>-->
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "FAQs"
}
</script>

<style scoped>
/* Tab content - closed */
.tab-content {
  max-height: 0;
  -webkit-transition: max-height .35s;
  -o-transition: max-height .35s;
  transition: max-height .35s;
}
/* :checked - resize to full height */
.tab input:checked ~ .tab-content {
  max-height: 100vh;
}
/* Label formatting when open */
.tab input:checked + label{
  /*@apply text-xl p-5 border-l-2 border-indigo-500 bg-gray-100 text-indigo*/
  font-size: 1.25rem; /*.text-xl*/
  padding: 1.25rem; /*.p-5*/
  border-left-width: 2px; /*.border-l-2*/
  border-color: #6574cd; /*.border-indigo*/
  background-color: #f8fafc; /*.bg-gray-100 */
  color: #6574cd; /*.text-indigo*/
}
/* Icon */
.tab label::after {
  float:right;
  right: 0;
  top: 0;
  display: block;
  width: 1.5em;
  height: 1.5em;
  line-height: 1.5;
  font-size: 1.25rem;
  text-align: center;
  -webkit-transition: all .35s;
  -o-transition: all .35s;
  transition: all .35s;
}
/* Icon formatting - closed */
.tab input[type=checkbox] + label::after {
  content: "+";
  font-weight:bold; /*.font-bold*/
  border-width: 1px; /*.border*/
  border-radius: 9999px; /*.rounded-full */
  border-color: #b8c2cc; /*.border-grey*/
}
.tab input[type=radio] + label::after {
  content: "\25BE";
  font-weight:bold; /*.font-bold*/
  border-width: 1px; /*.border*/
  border-radius: 9999px; /*.rounded-full */
  border-color: #b8c2cc; /*.border-grey*/
}
/* Icon formatting - open */
.tab input[type=checkbox]:checked + label::after {
  transform: rotate(315deg);
  background-color: #6574cd; /*.bg-indigo*/
  color: #f8fafc; /*.text-grey-lightest*/
}
.tab input[type=radio]:checked + label::after {
  transform: rotateX(180deg);
  background-color: #6574cd; /*.bg-indigo*/
  color: #f8fafc; /*.text-grey-lightest*/
}
</style>
