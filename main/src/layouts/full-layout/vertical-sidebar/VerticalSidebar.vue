<template>
  <aside
      class="left-sidebar"
      :class="
      Sidebar_drawer ? `show-sidebar bg-${SidebarColor}` : `bg-${SidebarColor}`
    "
  >
    <div :class="`bg-${logoColor} navbar-header`">
      <LogoDark/>
      <span
          class="d-block d-lg-none close-sidebar-btn"
          @click="showMobileSidebar"
      >
        <i class="mdi mdi-close font-22"></i>
      </span>
    </div>

    <div class="scrlbar">
      <ul class="nav flex-column mb-0">

        <b-dropdown
            variant="primary"
            id="dropdown-1"
            text="AccountController"
            class=""
        >

          <b-dropdown-item>
            <router-link :to="'/ui-elements/alert'" class="nav-link d-flex">
              GET /account/{id}
            </router-link>
          </b-dropdown-item>
          <b-dropdown-item>
            <router-link :to="'/ui-elements/alert'" class="nav-link d-flex">GET /account/get/{accountNo}</router-link>
          </b-dropdown-item>
          <b-dropdown-item>
            <router-link :to="'/ui-elements/alert'" class="nav-link d-flex">POST /account/save
            </router-link>
          </b-dropdown-item>
        </b-dropdown>

        <!--        <template v-for="(route, i) in routes">
                  &lt;!&ndash;-Single Menu &ndash;&gt;
                  <li class="nav-item" :key="i" v-if="!route.childern && !route.header">
                    <router-link :to="`${route.to}`" class="nav-link d-flex">
                      <i :class="route.icon"></i>
                      <span class="hide-text">{{ route.title }}</span>
                    </router-link>
                  </li>
                </template>-->
      </ul>
    </div>
  </aside>
</template>

<script>
import LogoDark from "../logo-dark/LogoDark";
import {mapState} from "vuex";
import SidebarData from "./SidebarData";

export default {
  name: "VerticalSidebar",
  components: {
    LogoDark,
  },
  data: () => ({
    initialShow: true,
    routes: SidebarData,
  }),
  computed: {
    ...mapState(["logoColor", "Sidebar_drawer", "SidebarColor"]),
    check() {
      return console.log(this.$router.history.current);
    },
  },
  methods: {
    showMobileSidebar() {
      this.$store.commit("SET_SIDEBAR_DRAWER", false);
    },
  },
};
</script>

<style>
</style>