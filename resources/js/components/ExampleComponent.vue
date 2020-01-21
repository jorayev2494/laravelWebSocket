<template>
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-md-8">
                <div class="card">
                    <div class="card-header">Example Component</div>

                    <div class="card-body">
                        I'm an example component. Test Universitet awd aw d Node Best awdawd Yakyb Test daw dwa 
                        a daw daw d a daw aw
                        a aw dadw aw aw daw aw d
                        aw d awdaw dawdaw daw daw 
                        awda wawd awd aw aw aw 
                        testsing node container watch-poll
                        not Alert();..55
                    </div>
                    <div>
                        {{ socketValue }}
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                socketValue: "Default Message!"
            }
        },
        mounted() {
            console.log('Component mounted.')
        },
        mounted() {
            // alert("Alertawd awd wad awdawd awd 111 22222 33");
            Echo.channel('home').listen('NewMessage', (event) => {
                this.socketValue += event.message;
            })
        },
    }
</script>
