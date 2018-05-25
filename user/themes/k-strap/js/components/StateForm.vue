<template>
    <div>
        <form class="form" >
            <div class="row">
                <div class="form-group col">
                    <label for="inputPassword2" class="sr-only">Select State</label>
                    <select v-model="state" class="custom-select">
                        <option selected>Select State</option>
                        <option v-for="location in locations" :key="location.slug" :value="location.route">{{ location.title }}</option>
                    </select>
                </div>
                <div class="form-group col-auto">
                    <button @click="routeForm($event)" type="submit" class="btn btn-secondary">GO</button>
                </div>
            </div>
        </form>
    </div>
</template>

<script>
    export default {
        props: {
            locationdata: {
                type: Object,
                default: {}
            }
        },
        data() {
            return {
                locations: {},
                state: {}
            }
        },
        mounted(){
            console.log(this.locationdata);
            this.locations = this.locationdata;
        },
        methods: {
            routeForm(e){
                e.preventDefault();
                window.location.href = this.state
            }
        }
    }
</script>