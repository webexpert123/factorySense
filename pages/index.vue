<template>
<div>
    <HeroHome />
    <HeroStats />
    <TrackAnything />
    <LogoCloud />
    <BuiltForEfficiency />
    <WhyCustomersChooseUs />
</div>
</template>

<script>
import HeroHome from '@/components/HeroHome'
import LogoCloud from '@/components/LogoCloud'
import TrackAnything from '@/components/TrackAnything'
import BuiltForEfficiency from '@/components/BuiltForEfficiency'
import HeroStats from '@/components/HeroStats'
import WhyCustomersChooseUs from '@/components/WhyCustomersChooseUs'
export default {
  name: "PageIndex",
  components: { HeroHome, LogoCloud, TrackAnything, BuiltForEfficiency, HeroStats, WhyCustomersChooseUs }
  // layout: 'abc' // by default it picks default.vue from layouts folder, it can be overridden here
}
</script>
