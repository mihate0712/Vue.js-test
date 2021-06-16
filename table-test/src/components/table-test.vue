<template>
    <div>
        <b-table striped hover :items="items"></b-table>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                items: [
                    {departure_time: '18:15', type: '新快速', destination: '京都方面湖西経由敦賀', delay: '平常運転中'},
                    {departure_time: '18:08', type: '快　速', destination: '京都方面米原', delay: '遅れ約10分'},
                    {departure_time: '18:02', type: '普　通', destination: '高　槻', delay: '遅れ約20分'},
                    {departure_time: '-', type: '丹波路快速', destination: '当駅止', delay: '平常運転中'},
                ]
            }
        }
    }
</script>