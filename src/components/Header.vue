<style scoped>
#header-menu-switch {
    display: none;
}

.header {
    height: 80px;
    display: flex;
    justify-content: center;
    margin: auto;
    padding: 0 1rem;
    position: relative;
    z-index: 9999;
}

.header-content {
    line-height: 80px;
}

.header-hb {
    display: none;
}

.header-nav {
    width: fit-content;
    display: flex;
}

.header-nav>ul {
    display: flex;
}

.header-list {
    align-self: center;
}

.header-list a {
    font-size: 18px;
    font-weight: 900;
    display: block;
    padding: 0rem 1.5rem;
    color: #FFFAFA;
    transition: all 0.3s linear;
}

.header-list a:hover {
    color: #C0C0C0;
}

.header-underline {
    width: 120px;
    height: 1px;
    display: none;
    margin: 0.5rem auto 1rem;
    background-color: #FFFAFA;
}

@media screen and (max-width: 1200px) {
    .header {
        padding: 0 2rem 0 1rem;
    }

    .header-hb {
        width: 30px;
        height: 45px;
        display: block;
        align-self: center;
        margin-left: auto;
        position: relative;
        cursor: pointer;
    }

    .header-hb-line {
        width: 32px;
        height: 2px;
        margin: auto;
        position: absolute;
        right: 0;
        left: 0;
        background-color: #FFFAFA;
        /* 線 */
        opacity: 1;
        transform: rotate(0deg);
    }

    .header-hb-line:nth-child(1) {
        top: 7px;
    }

    .header-hb-line:nth-child(2) {
        top: 19px;
    }

    .header-hb-line:nth-child(3) {
        top: 31px;
    }

    #header-menu-switch:checked+.header .header-hb-line:nth-child(1) {
        animation: hb-line-1 1s 1s forwards;
    }

    /* @keyframes hb-line-1 {
            0% {
                top: 7px;
                transform: rotate(0deg);
            }
        
            50% {
                top: 19px;
                transform: rotate(0deg);
            }
        
            100% {
                top: 19px;
                transform: rotate(405deg);
            }
        
        }
         */

    @keyframes hb-line-1 {
        0% {
            top: 7px;
            transform: rotate(0deg);
        }

        10% {
            top: 31px;
            transform: rotate(0deg);
        }

        20% {
            top: 7px;
            transform: rotate(0deg);
        }

        30% {
            top: 31px;
            transform: rotate(0deg);
        }

        40% {
            top: 7px;
            transform: rotate(0deg);
        }

        50% {
            top: 19px;
            transform: rotate(0deg);
        }

        75% {
            top: 19px;
            transform: rotate(-405deg);
        }

        100% {
            top: 19px;
            transform: rotate(405deg);
        }

    }

    #header-menu-switch:checked+.header .header-hb-line:nth-child(2) {
        animation: hb-line-2 1s 0s forwards;
    }

    /* @keyframes hb-line-2 {
            0% {
                opacity: 1;
            }
        
            100% {
                opacity: 0;
            }
        
        }
    */

    @keyframes hb-line-2 {
        0% {
            opacity: 1;
        }

        10% {
            opacity: 0;
        }

        20% {
            opacity: 1;
        }

        30% {
            opacity: 0;
        }

        40% {
            opacity: 1;
        }

        50% {
            opacity: 0;
        }

        60% {
            opacity: 1;
        }

        70% {
            opacity: 0;
        }

        80% {
            opacity: 1;
        }

        90% {
            opacity: 0;
        }

        100% {
            opacity: 0;
        }
    }

    #header-menu-switch:checked+.header .header-hb-line:nth-child(3) {
        animation: hb-line-3 1s 1s forwards;
    }

    /* @keyframes hb-line-3 {
            0% {
                top: 31px;
                transform: rotate(0deg);
            }
            50% {
                top: 19px;
                transform: rotate(0deg);
            }
            100% {
                top: 19px;
                transform: rotate(675deg);
            }
        } */

    @keyframes hb-line-3 {
        0% {
            top: 31px;
            transform: rotate(0deg);
        }

        10% {
            top: 7px;
            transform: rotate(0deg);
        }

        20% {
            top: 31px;
            transform: rotate(0deg);
        }

        30% {
            top: 7px;
            transform: rotate(0deg);
        }

        40% {
            top: 31px;
            transform: rotate(0deg);
        }

        50% {
            top: 19px;
            transform: rotate(0deg);
        }

        75% {
            top: 19px;
            transform: rotate(-675deg);
        }

        100% {
            top: 19px;
            transform: rotate(675deg);
        }
    }

    #header-menu-switch:checked+.header .header-nav {
        left: 0;
        opacity: 1;
        transition: opacity 1s 2s;
    }

    .header-nav {
        width: 100%;
        position: absolute;
        top: 80px;
        left: -100%;
        /* background-image: url("../assets/images/background.webp");
            background-size: cover; */
        background-color: #222223;
        opacity: 0;
        transition: opacity 1s 0s,
            left 0s 1s;
    }

    .header-nav>ul {
        width: 100%;
        display: block;
        float: left;
        /* float: right; */
    }

    .header-list a {
        display: flex;
        justify-content: space-between;
    }

    .header-underline {
        width: 0%;
        display: block;
        margin: 0 0 0.5rem;
        transition: all 1s linear;
    }

    .header-list:hover .header-underline {
        width: 100%;
    }
}

.title {
    font-family: "Henny Penny";
    font-size: 48px;
    font-weight: 900;
    width: fit-content;
    line-height: 180px;
    /* color: #26273B; */
    margin: auto;
}

.title h1 a {
    color: #FFFAFA;
    letter-spacing: 0.2rem;
}

.title h1 a:hover {
    color: #C0C0C0;
}

@media screen and (max-width: 1200px) {
    .title {
        font-size: 36px;
        line-height: 80px;
        position: relative;
        z-index: 10000;
        transform: translateY(-80px);
    }
}

@media screen and (max-width: 575px) {
    .title {
        font-size: 24px;
    }
}

@media screen and (max-width: 380px) {
    .title h1 a {
        letter-spacing: 0.1rem;
    }
}

@media screen and (max-width: 360px) {
    .title {
        margin: 0 5rem 0 1.5rem;
    }
}

.header-search {
    line-height: 30px;
    padding: 0rem 1.5rem;
}

.header-search-input {
    color: #FFFAFA;
    border: 1px #FFFAFA solid;
    padding: 0 0.25rem;
}

.header-search-button {
    color: #FFFAFA;
    border: 1px #FFFAFA solid;
    padding: 0rem 1rem;
    transition: all 0.3s linear;
}

.header-search-button:hover {
    color: #222223;
    background-color: #FFFAFA;
}

.header-search-lightbox {
    width: 100%;
    height: 100%;
    line-height: 2;
    color: #FFFFFF;
    background-color: #222223;
    ;
    display: flex;
    flex-direction: column;
    align-items: center;
    /* justify-content: center; */
    opacity: 0.95;
    overflow: auto;
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    z-index: 99999;
}

.header-search-lightbox div:nth-child(n+2) {
    margin-top: 1.5rem;
}

.header-search-lightbox div:last-child {
    margin-bottom: 5rem;
}

.header-search-lightboxSearch {
    width: fit-content;
    margin: 7.5rem 0 1.5rem 0;
}

.header-search-lightboxButton {
    line-height: 25px;
    color: #FFFAFA;
    display: block;
    /* border: 1px #FFFAFA solid; */
    margin-left: auto;
    padding: 0rem 0.5rem;
    transform: translate(35px, -5px);
    transition: all 0.3s linear;
}

.header-search-lightboxInput {
    width: 300px;
    line-height: 40px;
    color: #FFFAFA;
    border: 1px #FFFAFA solid;
    padding: 0 0.25rem;
}

.header-search-lightboxButton i {
    color: #FFFAFA;
    margin: auto;
    transition: all 0.3s linear;
}

.header-search-lightbox div:nth-child(n+2) {
    margin-top: 1rem;
}

@media screen and (max-width: 1200px) {
    .header-search {
        display: flex;
        justify-content: space-between;
        margin: 1.5rem 0;
    }
}

@media screen and (max-width: 768px) {
    .header-search-lightbox div:nth-child(n+2) a {
        font-size: 16px;
        text-align: center;
    }
}

@media screen and (max-width: 499px) {
    .header-search-lightboxButton {
        transform: translate(0, -10px);
    }
}
</style>

<template>
    <header>
        <input type="checkbox" name="" id="header-menu-switch">
        <div class="header">
            <!-- 漢堡 -->
            <label for="header-menu-switch" class="header-hb">
                <span class="header-hb-line"></span>
                <span class="header-hb-line"></span>
                <span class="header-hb-line"></span>
            </label>
            <!-- 選單 -->
            <div class="header-content">
                <nav class="header-nav">
                    <ul>
                        <li class="header-list">
                            <a href="About">
                                <p>About</p>
                            </a>
                            <span class="header-underline"></span>
                        </li>
                        <!-- <li class="header-list">
                            <a href="Side-Project">
                                <p>Side Project</p>
                            </a>
                            <span class="header-underline"></span>
                        </li> -->
                        <li class="header-list">
                            <a href="LeetCode">
                                <p>LeetCode</p>
                            </a>
                            <span class="header-underline"></span>
                        </li>
                        <li class="header-list">
                            <a href="Interview">
                                <p>Interview</p>
                            </a>
                            <span class="header-underline"></span>
                        </li>
                        <!-- <li class="header-list">
                            <a href="Question">
                                <p>LeetCode & Interview</p>
                            </a>
                            <span class="header-underline"></span>
                        </li> -->
                        <li class="header-list">
                            <a href="Article">
                                <p>Article</p>
                            </a>
                            <span class="header-underline"></span>
                        </li>
                        <li class="header-list">
                            <div v-if="!showLightbox" class="header-search">
                                <input class="header-search-input" v-model="state.searchInput" type="text" placeholder="Search Article">
                                <button class="header-search-button" @click="search, showLightbox = true">Search</button>
                            </div>
                            <div v-if="showLightbox" class="header-search-lightbox">
                                <div class="header-search-lightboxSearch">
                                    <button class="header-search-lightboxButton" @click="closeLightbox"><i class="fa-solid fa-x"></i></button>
                                    <input class="header-search-lightboxInput" v-model="state.searchInput" type="text" placeholder="Search Article">
                                </div>
                                <div v-for="content in filteredDivContentList" :key="content">
                                    <a :href="content.url">{{ content.text }}</a>
                                </div>
                            </div>
                            <span class="header-underline"></span>
                        </li>
                        <li class="header-list d-none">
                            <a href="Reference">
                                <p>Reference</p>
                            </a>
                            <span class="header-underline"></span>
                        </li>
                    </ul>
                </nav>
            </div>
        </div>
        <div class="title">
            <h1><a href="/">{{ Title }}</a></h1>
        </div>
    </header>
</template>

<script setup>
import { ref, reactive, onMounted, computed } from "vue"

const Title = ref("");
const showTitle = () => {
    const originalText = "Charmying Blog";
    let index = 0;
    const intervalId = setInterval(() => {
        Title.value += originalText[index];
        index++;
        if (index === originalText.length) {
            clearInterval(intervalId);
        }
    }, 250) // 控制每個字出現的時間間隔，單位為毫秒
}
onMounted(() => {
    showTitle();
})

// 搜尋文章 for 迴圈跑全部文章
const state = reactive({
    searchInput: "",
    divContentList: [
        { text: "什麼是 Binary Tree(二元樹)？", url: "Algorithm_Tree-and-BinaryTree" },
        { text: "什麼是 slot？", url: "VUE_slot" },
        { text: "什麼是 Agile、Scrum 和 Kanban？", url: "Chat_Agile-vs-Scrum-vs-Kanban" },
        { text: "什麼是 DFS 和 BFS？", url: "Algorithm_DFS-vs-BFS" },
        { text: "什麼是 IIFE？", url: "JS_IIFE" },
        { text: "什麼是 柯里化和反柯里化？", url: "Algorithm_Curry" },
        { text: "什麼是 豐田式管理？", url: "Chat_TPS" },
        { text: "什麼是 v-for？", url: "VUE_v-for-introduce" },
        { text: ":has() 和 :not() 偽類選擇器", url: "CSS_has-and-not" },
        { text: "【美食札記】京悅港式飲茶", url: "Food_King-Young" },
        { text: "sort() V.S. toSorted()", url: "JS_sort-vs-toSorted" },
        { text: "什麼是 半導體的黃光、蝕刻、擴散和薄膜？", url: "Chat_ICs-Photolithography-vs-Etching-vs-Diffusion-vs-Deposition" },
        { text: "什麼是 CSR 、 SSR 和 Hydration？", url: "WEB_CSR-vs-SSR-vs-Hydration" },
        { text: "【美食札記】冪x2 La Miette Pizza&Kitchen", url: "Food_La-Miette-Pizza&Kitchen" },
        { text: "【美食札記】貓匿 MAONI Brunch｜早餐｜早午餐｜輕食｜下午茶｜咖啡茶飲", url: "Food_Mao-Ni-Brunch" },
        { text: "什麼是 IoT(物聯網) 和 AIoT(人工智慧物聯網)？", url: "Chat_IoT-vs-AIoT" },
        { text: "什麼是 JavaScript 的 class？", url: "JS_class" },
        { text: "【美食札記】太初 麵食りようり", url: "Food_Tai-Chu" },
        { text: "【美食札記】軟蛋醬 蛋包飯專門製作所", url: "Food_SOFT-EGG" },
        { text: "Axios 攔截器(Axios Interceptors)", url: "JS_Axios-Interceptors" },
        { text: "【美食札記】島津和牛咖哩", url: "Food_SHIMADZU-Curry" },
        { text: "【美食札記】八庵壽司割烹", url: "Food_Ba-An-Sushi" },
        { text: "【美食札記】十二段鍋物堂", url: "Food_12sukiyak" },
        { text: "JavaScript 的 indexOf()", url: "JS_indexOf" },
        { text: "JavaScript 的模板字串插值(Template String Interpolation)", url: "JS_TemplateStringInterpolation" },
        { text: "JavaScript 中陣列(Array)的遍歷方法", url: "JS_traversal" },
        { text: "什麼是 迴圈、迭代、遍歷、遞迴？", url: "JS_Loop-vs-Iteration-vs-Traversal-vs-Recursion" },
        { text: "【美食札記】飯飯 一中店", url: "Food_Yi-Zhong-Fan-Fan" },
        { text: "【美食札記】台中公園路大麵𥺧", url: "Food_Gong-Yuan-Road-Da-Mian-Geng" },
        { text: "什麼是 賽局理論(Game Theory)？", url: "Chat_GameTheory-introduce" },
        { text: "【美食札記】平祿壽司", url: "/Food_Ping-Lu-Sushi" },
        { text: "【美食札記】阿如早餐店", url: "/Food_A-Ru" },
        { text: "【Pandas】Pandas DataFrame 處理雙維度資料方法", url: "/PY_Pandas-DataFrame" },
        { text: "【Pandas】Pandas Series 處理單維度資料方法", url: "/PY_Pandas-Series" },
        { text: "什麼是 遞迴(Recursion)？", url: "/Software_recursion" },
        { text: "bind V.S. call V.S. apply", url: "/JS_bind-vs-call-vs-apply" },
        { text: "什麼是 ODM、OEM、OBM 和 IDM？", url: "/Chat_ODM-vs-OEM-vs-OBM-vs-IEM" },
        { text: "什麼是 B2B、B2C、B2B2C 和 C2C？", url: "/Chat_B2B-vs-B2C-vs-B2B2C-vs-C2C" },
        { text: "Git 常用指令", url: "/Git_basic-instructions" },
        { text: "什麼是 WebSocket？", url: "/WEB_WebSocket-introduce" },
        { text: "stack(堆疊) V.S. queue(佇列)", url: "/JS_stack-vs-queue" },
        { text: "JavaScript 的正規表達式 (Regular Expression)", url: "/JS_RegularExpression" },
        { text: "什麼是 CORS？", url: "/WEB_CORS-introduce" },
        { text: "什麼是 Proxy？", url: "/WEB_Proxy-introduce" },
        { text: "什麼是 props？", url: "/VUE_props" },
        { text: "undefined V.S. undeclared V.S. null", url: "/JS_undefined-vs-undeclared-vs-null" },
        { text: "setAttribute V.S. getAttribute", url: "/JS_setAttribute-vs-getAttribute" },
        { text: "setTimeout V.S. setInterval", url: "/JS_setTimeout-vs-setInterval" },
        { text: "什麼是 解構賦值(Destructuring Assignment)？", url: "/JS_destructuring-assignment" },
        { text: "什麼是 OWASP？", url: "/WEB_OWASP-introduce" },
        { text: "陣列中的物件資料選取與排序", url: "/JS_sort" },
        { text: "什麼是 Event Bus？", url: "/VUE_eventBus" },
        { text: "如何建立 Vue-CLI？", url: "/VUE_createVUEcli" },
        { text: "什麼是 閉包(Closure)？", url: "/JS_closure" },
        { text: "事件捕獲(Capturing Events) V.S. 冒泡事件(Bubbling Events)", url: "/JS_BubblingEvents-vs-CapturingEvents" },
        { text: "JavaScript 的物件導向", url: "/JS_OOP" },
        { text: "By Value V.S. By Reference", url: "/JS_byValue-vs-byReference" },
        { text: "淺拷貝(Shallow Copy) V.S. 深拷貝(Deep Copy)", url: "/JS_shallowCopy-vs-deepCopy" },
        { text: "Vue 模板語法", url: "/VUE_syntax" },
        { text: "迴圈基礎 & 迴圈控制", url: "/PY_loop" },
        { text: "if 判斷式和簡易的四則運算", url: "/PY_arithmetic" },
        { text: "什麼是 CRUD？", url: "/DB_CRUD" },
        { text: "淺談網頁技術名詞", url: "/WEB_web-noun" },
        { text: "BOM V.S. DOM", url: "/Code_BOM-vs-DOM" },
        { text: "CSS 選取第一個、最後一個、偶數、奇數、第n個標簽元素", url: "/CSS_nth-child" },
        { text: "JavaScript 的非同步 (Asynchronous)", url: "JS_Asynchronous" },
        { text: "什麼是 AJAX？", url: "/JS_AJAX" },
        { text: "什麼是 CSS box-sizing？", url: "/CSS_box-sizing" },
        { text: "slice() V.S. splice() V.S. split()", url: "/JS_slice-vs-splice-vs-split" },
        { text: "delete V.S. splice", url: "/JS_delete-vs-splice" },
        { text: "var V.S. let V.S. const", url: "/JS_var-vs-let-vs-const" },
        { text: "什麼是 RESTful API？", url: "/WEB_RESTfulAPI-introduce" },
        { text: "什麼是 TCP/IP？", url: "/WEB_TCP-IP" },
        { text: "什麼是 SSL 和 TLS？", url: "/WEB_SSL-and-TLS" },
        { text: "HTTP V.S. HTTPS", url: "/WEB_HTTP-vs-HTTPS" },
        { text: "限制內容字數寬度或行數", url: "/Code_Limit-Line-Width" },
        { text: "map() V.S. forEach()", url: "/JS_map-vs-forEach" },
        { text: "MVC V.S. MVVM", url: "/WEB_MVC-vs-MVVM" },
        { text: "元件的生命週期與更新機制", url: "/VUE_LifeCycle" },
        { text: "Cookie V.S. LocalStorage V.S. SessionStorage", url: "/WEB_Cookie-vs-LocalStorage-vs-SessionStorage" },
        { text: "什麼是 API？", url: "/WEB_api-introduce" },
        { text: "什麼是 NPM？了解 node套件管理工具 npm install", url: "/WEB_npm-introduce" },
        { text: "什麼是 CDN？| CDN 的工作原理是什麼？", url: "/WEB_cdn-introduce" },
        { text: "HTML <code> 顯示程式碼內容", url: "/HTML_codeTag" },
        { text: "HTML 表格 (table)", url: "/HTML_tableTag" },
        { text: "【程式入門】該如何開始自學寫程式", url: "Programming-Language" },
    ],
});

const filteredDivContentList = computed(() => {
    if (state.searchInput) {
        const searchKeyword = state.searchInput.toLowerCase();
        return state.divContentList.filter(content =>
            content.text.toLowerCase().includes(searchKeyword)
        );
    } else {
        return state.divContentList;
    }
});

const showLightbox = ref(false);
const closeLightbox = () => {
    showLightbox.value = false;
};
</script>