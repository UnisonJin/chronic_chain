<template>
  <SpSidebar v-on:sidebar-open="sidebarOpen = true" v-on:sidebar-close="sidebarOpen = false">
    <template v-slot:default>
      <img src="../assets/logo.svg" class="app-logo" alt="logo" />
      <SpLinkIcon link="/" text="Dashboard" icon="Dashboard" />
      <SpLinkIcon link="/my-nft" text="My NFT's" icon="Modules" />
      <!--      <SpLinkIcon link="/my-nft" text="The OG" icon="Form" />-->
      <!--      <SpLinkIcon link="/my-nft" text="The Early Bird" icon="Form" />-->
      <!--      <SpLinkIcon link="/my-nft" text="MThe Executive" icon="Form" />-->
      <SpLinkIcon link="/blocks" text="Block Explorer" icon="Transactions" />
      <SpLinkIcon href="https://app.osmosis.zone/?from=ATOM&to=OSMO" text="Buy Now" icon="Token" />
      <!--      <SpLinkIcon link="/relayers" text="Relayers" icon="Transactions" />-->
      <div class="sp-dash"></div>
      <!--      <SpLinkIcon href="https://github.com/tendermint/starport" target="_blank" text="Documentation" icon="Docs" />-->
    </template>
    <!--    <template v-slot:footer>-->
    <!--      <SpStatusAPI :showText="sidebarOpen" />-->
    <!--      <SpStatusRPC :showText="sidebarOpen" />-->
    <!--      <SpStatusWS :showText="sidebarOpen" />-->
    <!--      <div class="sp-text">Build: v0.3.8</div>-->
    <!--    </template>-->
  </SpSidebar>
</template>

<style>
.sp-link-icon__text {
  color: #111;
}

.sp-link-icon .sp-link-icon-wrapper {
  opacity: 1;
}

.sp-sidebar {
  background-color: white;
}

.sp-fill {
  background-color: #555e75;
}

.sp-wallet .sp-button {
  background-color: #111;
}

.sp-token-send__header h3,
.sp-assets__header h3,
.sp-transfer-list__header h3,
.sp-relayers__header h3 {
  color: #111;
}

.sp-token-send__header span,
.sp-assets__header span,
.sp-transfer-list__header span,
.sp-relayers__header span {
  color: #f7f7ff;
}

.sp-sidebar__content .sp-icon:before {
  color: #555e75;
}

.sp-sidebar__footer .sp-status-api__text,
.sp-sidebar__footer .sp-status-rpc__text,
.sp-sidebar__footer .sp-status-ws__text {
  color: #555e75;
  opacity: 0.9;
}

.app-logo {
  width: 100%;
  margin-bottom: 3rem;
}

/*@media screen and (max-width: 768px) {*/
/*  .app-logo {*/
/*    left: 8.5rem;*/
/*    right: auto;*/
/*  }*/
/*}*/
</style>
<script>
export default {
  name: 'Sidebar',
  data() {
    return {
      sidebarOpen: true,
    }
  },
  computed: {
    hasWallet() {
      return this.$store.hasModule(['common', 'wallet'])
    },
  },
}
</script>
