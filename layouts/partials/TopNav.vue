<template>
    <div>
       
        <b-navbar toggleable="lg" type="light" variant="light">
             

            <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

            <b-collapse id="nav-collapse" is-nav>
            <b-navbar-nav>
                <b-nav-item href="/">Home</b-nav-item>
                <b-nav-item href="/dashboard"  >Dashboard</b-nav-item>
            </b-navbar-nav>

            <!-- Right aligned nav items -->
            <b-navbar-nav class="ml-auto">
                 

                  <b-navbar-nav>
                <b-nav-item href="/auth/login">Login</b-nav-item>
                <b-nav-item href="/auth/register"  >Register</b-nav-item>
            </b-navbar-nav>

                <b-nav-item-dropdown right>
                    
                <!-- Using 'button-content' slot -->
                <template #button-content>
                    <em>User</em>
                </template>
                <b-dropdown-item href="#">Profile</b-dropdown-item>
                <b-dropdown-item href="#">Sign Out</b-dropdown-item>
                </b-nav-item-dropdown>
            </b-navbar-nav>
            </b-collapse>
        </b-navbar>
    </div> 
</template>
 