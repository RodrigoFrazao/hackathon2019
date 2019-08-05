
<template>

    <v-stage :config="configstory"  >
        <v-layer>
            <v-text v-for="(item, index) in items" v-bind:key="item.message"
                    @dragstart="handleDragStart"
                    @dragend="handleDragEnd"
                    :config="{
            text: item.message,
            x: 0,
            y: 10+index*20,
            draggable: true,
            fill: isDragging ? 'green' : 'black'
          }"
            />
        </v-layer>
    </v-stage>

</template>

<script>
    export default {
        data() {
            return {
                configstory: {
                    width: 2000,
                    height: 2000,
                },
                items : [
                    {
                        message: 'NAPI',
                        stories: ['VO-1', 'VO-2'],
                    },
                    {
                        message: 'CAPI',
                        stories: ['VO-3', 'VO-4'],
                    },
                    {   message: 'Usermanagement',
                        stories: ['VO-5', 'VO-6'],
                    },
                    {   message: 'e-consult',
                        stories: ['VO-7', 'VO-8'],
                    },
                    {   message: 'PPAPI',
                        stories: ['VO-8', 'VO-9'],
                    },
                    {   message: 'ConsultUI',
                        stories: ['VO-10', 'VO-11'],
                    },
                ],
            };
        },
        methods: {
            handleDragStart() {
                this.isDragging = true;
            },
            handleDragEnd() {
                this.isDragging = false;

            },
        },
    };

</script>