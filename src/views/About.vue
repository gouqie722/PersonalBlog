<template>
    <div class="about">
        <BHeader></BHeader>
        <div class="content">
            <div class="content_left">
                <div class="description">
                    <div class="about_title">关于我</div>
                    <p>NodeNodeNodeNode</p>
                    <p>NodeNodeNodeNode</p>
                    <p>NodeNodeNodeNode</p>
                    <p>NodeNodeNodeNode</p>
                    <p>NodeNodeNodeNode</p>
                    <p>NodeNodeNodeNode</p>
                    <div class="about_title">关于博客</div>
                    <p>NodeNodeNodeNode</p>
                    <p>NodeNodeNodeNode</p>
                    <p>NodeNodeNodeNode</p>
                    <p>NodeNodeNodeNode</p>
                    <p>NodeNodeNodeNode</p>
                    <p>NodeNodeNodeNode</p>
                </div>
                <div class="blog_comments">
                    <span class="blog_comments_msg">关于：目前有66 条留言</span>
                    <div class="blog_comment">
                        <span>
                            <b>许寒</b>：发表于 2019年02月13日 20:49[回复]
                        </span>
                        <div>PHP是世界上最好的语言</div>
                    </div>
                    <div class="blog_comment">
                        <span>
                            <b>许寒</b>：发表于 2019年02月13日 20:49[回复]
                        </span>
                        <div>PHP是世界上最好的语言</div>
                    </div>
                    <div class="blog_comment">
                        <span>
                            <b>许寒</b>：发表于 2019年02月13日 20:49[回复]
                        </span>
                        <div>PHP是世界上最好的语言</div>
                    </div>
                    <div class="blog_comment">
                        <span>
                            <b>许寒</b>：发表于 2019年02月13日 20:49[回复]
                        </span>
                        <div>PHP是世界上最好的语言</div>
                    </div>
                    <div class="blog_comment">
                        <span>
                            <b>许寒</b>：发表于 2019年02月13日 20:49[回复]
                        </span>
                        <div>PHP是世界上最好的语言</div>
                    </div>
                    <div class="blog_comment">
                        <span>
                            <b>许寒</b>：发表于 2019年02月13日 20:49[回复]
                        </span>
                        <div>PHP是世界上最好的语言</div>
                    </div>
                </div>
            </div>
            <div class="content_right">
                <div class="right_module">
                    <div>随机标签云</div>
                    <a href="" v-for="(item, index) in randomTags" :key="index" :style="{color: randomColor(), fontSize: randomSize()}">{{item.tag}}</a>

                </div>
                <div class="right_module">
                    <div>最近热门</div>
                    <ul>
                        <li><a href="">使用码云git的web实现生产环境代</a></li>
                        <li><a href="">使用码云git的web实现生产环境代</a></li>
                        <li><a href="">使用码云git的web实现生产环境代</a></li>
                        <li><a href="">使用码云git的web实现生产环境代</a></li>
                        <li><a href="">使用码云git的web实现生产环境代</a></li>
                        <li><a href="">使用码云git的web实现生产环境代</a></li>
                    </ul>
                </div>
                <div class="right_module">
                    <div>最新评论</div>
                    <ul>
                        <li>
                            <div>
                                <span>萌新</span>
                                <span class="pull_right">这里是时间</span>
                            </div>
                            <p>啊不知道是不是因为带了链接被插件屏蔽</p>
                        </li>
                        <li>
                            <div>
                                <span>萌新</span>
                                <span class="pull_right">这里是时间</span>
                            </div>
                            <p>啊不知道是不是因为带了链接被插件屏蔽</p>
                        </li>
                        <li>
                            <div>
                                <span>萌新</span>
                                <span class="pull_right">这里是时间</span>
                            </div>
                            <p>啊不知道是不是因为带了链接被插件屏蔽</p>
                        </li>
                        <li>
                            <div>
                                <span>萌新</span>
                                <span class="pull_right">这里是时间</span>
                            </div>
                            <p>啊不知道是不是因为带了链接被插件屏蔽</p>
                        </li>
                        <li>
                            <div>
                                <span>萌新</span>
                                <span class="pull_right">这里是时间</span>
                            </div>
                            <p>啊不知道是不是因为带了链接被插件屏蔽</p>
                        </li>
                        <li>
                            <div>
                                <span>萌新</span>
                                <span class="pull_right">这里是时间</span>
                            </div>
                            <p>啊不知道是不是因为带了链接被插件屏蔽</p>
                        </li>
                    </ul>
                </div>
                <div class="right_module">
                    <div>友情链接</div>
                    <span><a href="#">挨踢茶馆</a></span><span><a href="#">挨踢茶馆</a></span>
                    <span><a href="#">挨踢茶馆</a></span><span><a href="#">挨踢茶馆</a></span>
                    <span><a href="#">挨踢茶馆</a></span><span><a href="#">挨踢茶馆</a></span>
                    <span><a href="#">挨踢茶馆</a></span><span><a href="#">挨踢茶馆</a></span>
                    <span><a href="#">挨踢茶馆</a></span><span><a href="#">挨踢茶馆</a></span>

                </div>
            </div>
        </div>
        <BFooter></BFooter>
    </div>
</template>
<script>
import BHeader from '../components/index/header.vue';
import BFooter from '../components/index/footer.vue';
import { mapState } from 'vuex'
export default {
    components: {
        BHeader,
        BFooter
    },
    computed: {
        ...mapState(['randomTags'])
    },
    methods: {
        randomColor(){
            var red = Math.random() * 255;
            var green = Math.random() * 255;
            var blue = Math.random() * 255;
            return `rgb(${red}, ${green}, ${blue})`;
        },
        randomSize(){
            var size = Math.random() * 20 + 12 + "px";
            return size; 
        }
    }
}
</script>
<style lang="less">
    @import '../less/about.less';
</style>