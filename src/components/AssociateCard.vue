<template>
    <div style="color: #BEAF67;" class="mx-auto mx-md-5 mt-lg-5">
        <div class="pa-0 text-h6 text-md-h5 text-center mb-1" style="color: #0e5c60;">{{ lawyer.name }}</div>
        <div class="" style="color:#0A4770">
            <div class="h6 rounded-t-lg pt-1" style="background-color: #BEAF67; color: white; display:block;" >{{ englishOn? lawyer.title[1] : lawyer.title[0] }}</div>
        </div>
        <div
            class="custom-border customFrame mx-auto"
            :style="$vuetify.breakpoint.md || $vuetify.breakpoint.lg || $vuetify.breakpoint.xl ? 'width: 350px' : 'width: 300px'">
            <v-img
            eager
            :src="lawyer.pic"
            :height="$vuetify.breakpoint.md || $vuetify.breakpoint.lg || $vuetify.breakpoint.xl ? 450 : 445"
            :max-width="$vuetify.breakpoint.md || $vuetify.breakpoint.lg || $vuetify.breakpoint.xl ? 400 : 342"></v-img>
        </div>
        <div class="d-flex justify-space-between mx-auto my-2">
            <div class="d-flex justify-start" style="color:#0A4770">
            </div>
            <div class="d-flex justify-end">
                <v-btn color="#0e5c60" dark plain class="mr-5 font-weight-bold button" :href="lawyer.href1" :target="lawyer.target"> Email </v-btn>
                <v-btn color="#BEAF67" dark outlined class="rounded-br-xl font-weight-bold button rounded-sm custom-border" :href="lawyer.href2"> {{ englishOn ? 'Call' : 'Hívás'}} </v-btn>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'AssociateCard',
    props: ['lawyer', 'englishOn'],
    data(){
        return {

        }
    }
}
</script>