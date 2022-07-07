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
      <ul class="nav flex-column mb-0 pd-5">
        <b-dropdown
            variant="primary"
            id="dropdown-1"
            text="Account Controller"
            class="dropdown-text"
        >
          <b-dropdown-item>
            <router-link :to="'/ui-elements/alert'" class="nav-link d-flex href-text">
              GET /account/{id}
            </router-link>
          </b-dropdown-item>
          <b-dropdown-item>
            <router-link :to="'/ui-elements/alert'" class="nav-link d-flex href-text">
              GET /account/get/{accountNo}
            </router-link>
          </b-dropdown-item>
          <b-dropdown-item>
            <router-link :to="'/ui-elements/alert'" class="nav-link d-flex href-text">
              POST /account/save
            </router-link>
          </b-dropdown-item>
        </b-dropdown>
      </ul>

      <ul class="nav flex-column mb-0 pd-5">
        <b-dropdown
            variant="primary"
            id="dropdown-1"
            text="Authority Controller"
            class="dropdown-text"
        >
          <b-dropdown-item>
            <router-link :to="'/ui-elements/alert'" class="nav-link d-flex href-text">
              GET /authority
            </router-link>
          </b-dropdown-item>
          <b-dropdown-item>
            <router-link :to="'/ui-elements/alert'" class="nav-link d-flex href-text">
              GET /authority/{code}
            </router-link>
          </b-dropdown-item>
          <b-dropdown-item>
            <router-link :to="'/ui-elements/alert'" class="nav-link d-flex href-text">
              PUT /update/{authorityId}
            </router-link>
          </b-dropdown-item>
        </b-dropdown>
      </ul>

      <ul class="nav flex-column mb-0 pd-5">
        <b-dropdown
            variant="primary"
            id="dropdown-1"
            text="Contract Action Controller"
            class="dropdown-text"
        >
          <b-dropdown-item>
            <router-link :to="'/ui-elements/alert'" class="nav-link d-flex href-text">
              GET /contract-action
            </router-link>
          </b-dropdown-item>
        </b-dropdown>
      </ul>

      <ul class="nav flex-column mb-0 pd-5">
        <b-dropdown
            variant="primary"
            id="dropdown-1"
            text="Contract Controller"
            class="dropdown-text"
        >
          <b-dropdown-item>
            <router-link :to="'/ui-elements/alert'" class="nav-link d-flex href-text">
              POST /addNewContract
            </router-link>
          </b-dropdown-item>
          <b-dropdown-item>
            <router-link :to="'/ui-elements/alert'" class="nav-link d-flex href-text">
              GET /applyLs
            </router-link>
          </b-dropdown-item>
          <b-dropdown-item>
            <router-link :to="'/ui-elements/alert'" class="nav-link d-flex href-text">
              DELETE /deleteContract
            </router-link>
          </b-dropdown-item>
          <b-dropdown-item>
            <router-link :to="'/ui-elements/alert'" class="nav-link d-flex href-text">
              DELETE /delete/agreement
            </router-link>
          </b-dropdown-item>
          <b-dropdown-item>
            <router-link :to="'/ui-elements/alert'" class="nav-link d-flex href-text">
              GET /getContract
            </router-link>
          </b-dropdown-item>
          <b-dropdown-item>
            <router-link :to="'/ui-elements/alert'" class="nav-link d-flex href-text">
              POST /update/state
            </router-link>
          </b-dropdown-item>
          <b-dropdown-item>
            <router-link :to="'/ui-elements/alert'" class="nav-link d-flex href-text">
              PUT /update/{contractId}
            </router-link>
          </b-dropdown-item>
        </b-dropdown>
      </ul>
      <ul class="nav flex-column mb-0 pd-5">
        <b-dropdown
            variant="primary"
            id="dropdown-1"
            text="Cpv Controller"
            class="dropdown-text"
        >
          <b-dropdown-item>
            <router-link :to="'/ui-elements/alert'" class="nav-link d-flex href-text">
              POST /save
            </router-link>
          </b-dropdown-item>
          <b-dropdown-item>
            <router-link :to="'/ui-elements/alert'" class="nav-link d-flex href-text">
              POST /save/query
            </router-link>
          </b-dropdown-item>
        </b-dropdown>
      </ul>
      <ul class="nav flex-column mb-0 pd-5">
        <b-dropdown
            variant="primary"
            id="dropdown-1"
            text="Eo Awarding Controller"
            class="dropdown-text"
        >
          <b-dropdown-item>
            <router-link :to="'/ui-elements/alert'" class="nav-link d-flex href-text">
              POST /save
            </router-link>
          </b-dropdown-item>
          <b-dropdown-item>
            <router-link :to="'/ui-elements/alert'" class="nav-link d-flex href-text">
              POST /save/query
            </router-link>
          </b-dropdown-item>
        </b-dropdown>
      </ul>
      <ul class="nav flex-column mb-0 pd-5">
        <b-dropdown
            variant="primary"
            id="dropdown-1"
            text="Exel Export Controller"
            class="dropdown-text"
        >
          <b-dropdown-item>
            <router-link :to="'/ui-elements/alert'" class="nav-link d-flex href-text">
              POST /export
            </router-link>
          </b-dropdown-item>
        </b-dropdown>
      </ul>
      <ul class="nav flex-column mb-0 pd-5">
        <b-dropdown
            variant="primary"
            id="dropdown-1"
            text="Plan Controller"
            class="dropdown-text"
        >
          <b-dropdown-item>
            <router-link :to="'/ui-elements/alert'" class="nav-link d-flex href-text">
              POST /change
            </router-link>
          </b-dropdown-item>
          <b-dropdown-item>
            <router-link :to="'/ui-elements/alert'" class="nav-link d-flex href-text">
              POST /migrate
            </router-link>
          </b-dropdown-item>
          <b-dropdown-item>
            <router-link :to="'/ui-elements/alert'" class="nav-link d-flex href-text">
              POST /save
            </router-link>
          </b-dropdown-item>
        </b-dropdown>
      </ul>
      <ul class="nav flex-column mb-0 pd-5">
        <b-dropdown
            variant="primary"
            id="dropdown-1"
            text="Program Controller"
            class="dropdown-text"
        >
          <b-dropdown-item>
            <router-link :to="'/ui-elements/alert'" class="nav-link d-flex href-text">
              GET /{id}
            </router-link>
          </b-dropdown-item>
          <b-dropdown-item>
            <router-link :to="'/ui-elements/alert'" class="nav-link d-flex href-text">
              GET /like
            </router-link>
          </b-dropdown-item>
          <b-dropdown-item>
            <router-link :to="'/ui-elements/alert'" class="nav-link d-flex href-text">
              POST /save
            </router-link>
          </b-dropdown-item>
          <b-dropdown-item>
            <router-link :to="'/ui-elements/alert'" class="nav-link d-flex href-text">
              POST /update/{id}
            </router-link>
          </b-dropdown-item>
        </b-dropdown>
      </ul>
      <ul class="nav flex-column mb-0 pd-5">
        <b-dropdown
            variant="primary"
            id="dropdown-1"
            text="Supplier Controller"
            class="dropdown-text"
        >
          <b-dropdown-item>
            <router-link :to="'/ui-elements/alert'" class="nav-link d-flex href-text">
              GET /name
            </router-link>
          </b-dropdown-item>
          <b-dropdown-item>
            <router-link :to="'/ui-elements/alert'" class="nav-link d-flex href-text">
              GET /taxpayerId
            </router-link>
          </b-dropdown-item>
          <b-dropdown-item>
            <router-link :to="'/ui-elements/alert'" class="nav-link d-flex href-text">
              PUT /update
            </router-link>
          </b-dropdown-item>
        </b-dropdown>
      </ul>
      <ul class="nav flex-column mb-0 pd-5">
        <b-dropdown
            variant="primary"
            id="dropdown-1"
            text="Tender Controller"
            class="dropdown-text"
        >
          <b-dropdown-item>
            <router-link :to="'/ui-elements/alert'" class="nav-link d-flex href-text">
              POST /delete
            </router-link>
          </b-dropdown-item>
          <b-dropdown-item>
            <router-link :to="'/ui-elements/alert'" class="nav-link d-flex href-text">
              GET /getTender
            </router-link>
          </b-dropdown-item>
          <b-dropdown-item>
            <router-link :to="'/ui-elements/alert'" class="nav-link d-flex href-text">
              POST /makeTenderEditable
            </router-link>
          </b-dropdown-item>
        </b-dropdown>
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
.dropdown-text {
  font-family: inherit;
  font-size: 16px;
  letter-spacing: 1px;
}

.dropdown-item {
  padding: 1px;
  width: 100%;
}

.dropdown-menu{
  width: 100%;
}

.href-text{
  color: #48A3EA;
  font-family: inherit;
}

.href-text:hover{
  color: #48A3EA;
}

.pd-5{
  padding: 5px;
}
</style>