<template>
<div>
    <div class="div_news_rows" >
        <span class="mr-2" style="font-size: 28px; float :left;">
            <i class="fas fa-arrow-circle-right"></i>
        </span>
        <h3 class="ml-10">
            <router-link :to="'/show/' + item.show_id">{{ item.title }}
            </router-link>       
        </h3> 
    </div>
    <div>
        <ul class="ul_time_box">
        <li>
            <p class="mb-0">
                <span class="mr-2" style="font-size: 20px;">
                    <i class="far fa-calendar"></i>
                </span>
                {{ item.created_at }} , ID: {{item.id}}
            </p>
            <div v-if="item.category.name!=''">
                <span class="mr-2" style="font-size: 20px;">
                    <i class="fas fa-folder"></i> {{ item.category.name }}
                </span>
            </div>
        </li>
        </ul>
    </div>
    <hr class="hr_ex1"  />
</div>
</template>

<!-- -->
<script>
import {Mixin} from '../../mixin'

export default {
    mixins:[Mixin],
    props: ['item'],
    created (){},
}
</script>

