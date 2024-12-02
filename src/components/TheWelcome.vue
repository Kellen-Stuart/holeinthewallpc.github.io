<script setup lang="ts">
import WelcomeItem from './WelcomeItem.vue'
import DocumentationIcon from './icons/IconDocumentation.vue'
import ToolingIcon from './icons/IconTooling.vue'
import EcosystemIcon from './icons/IconEcosystem.vue'
import CommunityIcon from './icons/IconCommunity.vue'
import SupportIcon from './icons/IconSupport.vue'
</script>

<template>
  <WelcomeItem>
    <template #icon>
      <DocumentationIcon />
    </template>
    <template #heading>Why us?</template>
    <h3>Custom PCs</h3>

    We specialize in building custom pre-built PCs tailored to your specific needs, from gaming to productivity.
    
    <h3>Affordable Pricing</h3>

    Get high-quality PCs at competitive prices. We offer both new and used options to fit your budget.

    <h3>Local Expertise</h3>

    Serving the Kalispell area, we provide personalized service and support for your PC needs.
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <ToolingIcon />
    </template>
    <template #heading>Shop Pre-Built PCs</template>
    Browse our inventory of ready-to-use PCs, including gaming systems, budget builds, and refurbished models.
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <EcosystemIcon />
    </template>
    <template #heading>Contact Us</template>
    Have questions or want to discuss your custom build?
    Reach out today!
    <br/>
    📧 Email: support@holeinthewallpc.com
    <br/>
    📞 Phone: (406) 219-7936
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <CommunityIcon />
    </template>
    <template #heading>Services</template>
    Custom Builds: Let us assemble the perfect PC for you.
    <br/>
    Refurbished PCs: Budget-friendly options with guaranteed performance.
    <br/>
    Upgrades: Enhance your existing system with new components.
    <br/>
    Repair: We provide a repair service for PCs that are acting up.
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <SupportIcon />
    </template>
    <template #heading>Customer Reviews</template>
    ⭐️⭐️⭐️⭐️⭐️<br/>
    <i>"Hole in the Wall PCs built me an amazing gaming rig! Highly recommend them."</i><br/>
    - Alex, Kalispell
  </WelcomeItem>
</template>
