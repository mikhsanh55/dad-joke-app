<template>
    <div>
        <b-navbar toggleable="lg" type="dark" variant="dark">
            <b-navbar-brand href="/">{{title}}</b-navbar-brand>

            <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

            <b-collapse id="nav-collapse" is-nav>
            </b-collapse>
        </b-navbar>
        </div>
</template>
<script>
    import {BNavbar, BCollapse, BNavbarNav, BDropdownItem, BNavItemDropdown, BNavForm, BFormInput, BNavToggle} from 'bootstrap-vue'
    export default {
        props: ['title'],
        components: {
            BNavbar, BCollapse, BNavbarNav, BDropdownItem, BNavItemDropdown, BNavForm, BFormInput, BNavToggle
        }
    }
</script>