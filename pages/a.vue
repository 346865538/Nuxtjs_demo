<template>
    <div>
        
    </div>
</template>

<script>
    import axios from 'axios';
    import qs from 'qs';
    export default {
        // async asyncData ({ app, params }) {
        //     // return axios({
        //     //     method: 'get',
        //     //     url: 'https://api.github.com/users'
        //     // })
        //     // .then(function (res) {
        //     //     console.log(res.data)
        //     //     return { info: res.data };
        //     //     error(params)
        //     // })
        //     // let res = await app.$axios({
        //     //     url: '/personalCenterHandler/common/PersonalCenterCommonHandler.ashx?act=getLoginTypeData',
        //     //     method: 'get',
        //     //     headers: {
        //     //         'Content-Type': 'application/x-www-form-urlencoded; charset=UTF-8'
        //     //     }
        //     // })
        //     // return { info: JSON.stringify(res) }
        // },
        data () {
            return {
                a: 'a',
            }
        },
        async mounted () {
             let res = await this.$axios({
                url: '/personalCenterHandler/common/PersonalCenterCommonHandler.ashx',
                method: 'post',
                data: qs.stringify({
                    act: 'getLoginTypeData'
                }),
                headers: {
                    'Content-Type': 'application/x-www-form-urlencoded; charset=UTF-8'
                }
            })

            console.log(res)

        },
    }
</script>

<style>

</style>
