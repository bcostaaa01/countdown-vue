<template>
  <div>
    <h1>{{ heading }}</h1>

    <vue-countdown
      :time="54 * 24 * 60 * 60 * 1000"
      v-slot="{ days, hours, minutes, seconds }"
    >
      {{ days }} dagen, {{ hours }} huren, {{ minutes }} minuten en {{ seconds }} seconden
    </vue-countdown> 
<br>
<br>
    <img src="https://images0.persgroep.net/rcs/FzPSQAAzi0m-mCgUXcImyDbPUSQ/diocontent/160661570/_fitwidth/694/?appId=21791a8992982cd8da851550a453bd7f&quality=0.8" alt="Sinterklaas in Leiden, 2019" style="display: block; margin-left: auto; margin-right: auto; width: 50%;">
  </div>
</template>

<script>
import VueCountdown from "@chenfengyuan/vue-countdown";

export default {
  name: "CountdownComponent",
  components: {
    VueCountdown
  },
  data() {
    return {
      heading: "Hoeveel dagen tot Sinterklaas?",
    };
  },
};
</script>
