<script>
export default {
    props: {
        type: {
            type: String,
            default: 'default'
        },
        isDisabled: {
            type: Boolean,
            default: false
        }
    }
    // computed:{
    //     btnClasses(){
    //         switch (this.type){
    //             case 'primary':
    //                 return 'bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded';
    //                 case 'secondary':
    //                 return 'bg-green-500 hover:bg-green-700 text-white font-bold py-2 px-4 rounded';
    //                 case 'warning':
    //                 return 'bg-yellow-500 hover:bg-yellow-700 text-white font-bold py-2 px-4 rounded';
    //                 case 'info':
    //                 return 'bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded';
    //                 case 'danger':
    //                 return 'bg-red-500 hover:bg-red-700 text-white font-bold py-2 px-4 rounded';
    //             default:
    //                 return 'bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded';

    //         }
    //     }
    // }
}
</script>

<template>
    <button :class="{
        'font-semibold py-2 px-4 rounded border ': true,
        ' bg-blue-500 hover:bg-blue-700 text-white': type === 'primary',
        'bg-green-500 hover:bg-green-700 text-white': type === 'secondary',
        'bg-yellow-500 hover:bg-yellow-700 text-white': type === 'warning',
        'bg-blue-500 hover:bg-blue-700 text-white': type === 'info',
        'bg-red-500 hover:bg-red-700 text-white': type === 'danger',
        'bg-gray-500 hover:bg-gray-700 text-white': type === 'default',
    }" :disabled="isDisabled">
        <slot></slot>
    </button>
</template>