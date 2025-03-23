<template>
  <div class="w-full overflow-hidden text-gray-200 bg-zinc-900">
    <!-- 固定导航栏 -->
    <nav class="fixed top-0 left-0 right-0 z-50 w-full shadow-lg bg-zinc-950">
      <div class="flex items-center justify-between px-8 py-4">
        <div class="text-xl font-bold">
          🌸一朵顷刻绢花品牌
          <span class="text-sm text-gray-400">(DESIGNED BY LIUYOUXU)</span>
        </div>
        <ul class="flex space-x-6">
          <li>
            <a
              href="#"
              class="transition hover:text-blue-400"
              :class="{ 'font-bold text-blue-400': isHomePage }"
              @click="
                isHomePage = true;
                isProductPage = false;
                isCommunityPage = false;
                isCustomPage = false;
              "
            >
              首页
            </a>
          </li>
          <li>
            <a
              href="#product-section"
              class="transition hover:text-blue-400"
              :class="{ 'font-bold text-blue-400': isProductPage }"
              @click="
                isHomePage = false;
                isProductPage = true;
                isCommunityPage = false;
                isCustomPage = false;
              "
            >
              产品
            </a>
          </li>
          <li>
            <a
              href="#community-section"
              class="transition hover:text-blue-400"
              :class="{ 'font-bold text-blue-400': isCommunityPage }"
              @click="
                isHomePage = false;
                isProductPage = false;
                isCommunityPage = true;
                isCustomPage = false;
              "
            >
              社区
            </a>
          </li>
          <li>
            <a
              href="#"
              class="transition hover:text-blue-400"
              :class="{ 'font-bold text-blue-400': isCustomPage }"
              @click="
                isHomePage = false;
                isProductPage = false;
                isCommunityPage = false;
                isCustomPage = true;
              "
            >
              定制
            </a>
          </li>
        </ul>
      </div>
    </nav>
    <!-- 主区域 -->
<section
  class="flex flex-col items-stretch w-full min-h-screen mt-0 md:flex-row"
  v-if="isHomePage"
  style="
    background: linear-gradient(135deg, #2a241c, #4b4034 30%, #2a241c 70%);
  "
>
  <div
    class="w-full bg-center bg-cover md:w-1/2"
    style="background-image: url('/images/首页.jpg')"
  ></div>
  <div
    class="flex flex-col justify-center w-full px-12 py-16 md:w-1/2 md:px-20"
  >
    <h1 class="mb-6 text-6xl font-bold">一朵顷刻</h1>
    <p class="mb-8 text-2xl font-bold">
      融合传统工艺与现代设计，探索你的专属之美。
    </p>
    <p class="mb-8 text-sm text-left font-microsoftYaHei">
      <a
        href="https://www.ihchina.cn/project_details/14174" 
        target="_blank"
        class="relative block p-4 transition-all rounded-lg shadow-lg cursor-pointer bg-zinc-700 hover:scale-105 group"
        style="
          background: linear-gradient(
            120deg,
            #cc2d00,
            #cc6600 45%,
            #cc9900 75%
          );
        "
      >
        <span class="transition-colors group-hover:text-black">
          绢花，作为中国传统工艺之一，经过千年的传承与创新，融合了细腻的手工技巧和丰富的文化内涵。每一朵绢花都凝聚了艺术家的心血与创意，不仅是美的象征，更承载着深厚的文化底蕴。<br />
          绢花的制作工艺源远流长，早在汉代便已萌芽，而到了唐宋时期，绢花工艺达到了顶峰。如今，绢花不仅用于装饰，也常被用于礼仪场合、婚礼和传统节庆中，象征着美好与祝福。每一朵绢花都是匠人们辛勤创作的结晶，它们通过精湛的技艺将丝绸的柔美与自然的生命力巧妙结合，展现了工艺与艺术的完美融合。
        </span>
        <span class="absolute text-xs text-black bottom-2 right-2">
          点击跳转至中非遗产数字博物馆页面
        </span>
      </a>
    </p>
    <button
      class="px-6 py-3 text-xl font-bold text-yellow-500 transition-all transform bg-black rounded-full shadow-lg font-microsoftYaHei hover:bg-gray-800 hover:scale-110 hover:shadow-2xl"
      @click="
        isHomePage = false;
        isProductPage = true;
      "
    >
      立即探索
    </button>
  </div>
</section>

    <!-- 产品区 -->
    <section
      id="product-section"
      class="flex flex-col items-stretch w-full py-20 bg-zinc-900"
      v-if="isProductPage"
      style="
        background: linear-gradient(135deg, #2a241c, #4b4034 30%, #2a241c 70%);
      "
    >
      <div class="flex flex-col justify-center w-full px-12 md:px-16">
        <h2 class="mb-4 text-4xl font-bold">🌸 绢花工艺</h2>
        <p class="text-lg">
          绢花工艺源于千年历史，结合现代设计，为您带来前所未有的美感体验。
        </p>
        <!-- 修改后的按钮容器 -->
        <div class="flex justify-center w-full mt-6 space-x-6">
          <a
            href="https://shop.jd.com/your-shop-id.html"
            target="_blank"
            class="px-6 py-3 text-xl font-bold text-yellow-500 transition-all transform bg-black rounded-full shadow-lg hover:bg-gray-800 hover:scale-110 hover:shadow-2xl"
            style="border-radius: 25px"
          >
            查看京东店铺
          </a>
          <a
            href="https://shop.taobao.com/your-shop-id.html"
            target="_blank"
            class="px-6 py-3 text-xl font-bold text-yellow-500 transition-all transform bg-black rounded-full shadow-lg hover:bg-gray-800 hover:scale-110 hover:shadow-2xl"
            style="border-radius: 25px"
          >
            查看淘宝店铺
          </a>
        </div>
      </div>
      <!-- 修改后的产品展示容器 - 使用单一数组 -->
      <div
        class="grid w-full grid-cols-2 gap-6 px-8 mt-8 sm:grid-cols-3 md:grid-cols-6"
      >
        <a
          v-for="(product, idx) in allProducts"
          :key="idx"
          :href="product.link"
          target="_blank"
          class="p-2 transition-transform shadow-lg cursor-pointer rounded-xl hover:scale-105"
          style="
            background: radial-gradient(
              circle at 20% 20%,
              #662200,
              /* 深赤褐色基底 */ #994400 35%,
              /* 暗橙红色过渡 */ #cc5500 60%,
              /* 深陶土色主体 */ #662200 90% /* 回归深色收尾 */
            );
          "
        >
          <img :src="product.image" class="mb-4 rounded-lg" />
          <h3 class="font-semibold text-white">{{ product.name }}</h3>
          <p class="text-sm text-gray-300">{{ product.description }}</p>
        </a>
      </div>
    </section>
    <!-- 社区区 -->
    <section
      id="community-section"
      class="w-full py-10 bg-zinc-900 section-container"
      v-if="isCommunityPage"
      style="
        background: linear-gradient(135deg, #2a241c, #4b4034 30%, #2a241c 70%);
      "
    >
      <div class="max-w-6xl px-4 mx-auto">
        <div class="mb-10 text-center">
          <h2 class="mb-6 text-4xl font-bold">加入我们的社区</h2>
          <p class="mb-4 text-lg">
            在这里，您可以分享您的绢花创意，与其他爱好者交流。
          </p>
        </div>

        <!-- 百度贴吧嵌入 -->
        <div class="overflow-hidden bg-white rounded-lg shadow-xl">
          <div
            class="p-4 text-white bg-gradient-to-r from-amber-700 to-amber-900"
          >
            <h3 class="text-xl font-bold">绢花爱好者社区</h3>
            <p class="text-sm">分享您的作品、交流技艺、寻找灵感</p>
          </div>

          <!-- 百度贴吧嵌入iframe -->
          <iframe
            id="tieba-embed-frame"
            class="w-full"
            style="height: 800px"
            src="https://tieba.baidu.com/f?kw=绢花"
            frameborder="0"
          ></iframe>
        </div>

        <!-- 社区活动部分 -->
        <div class="grid grid-cols-1 gap-6 mt-12 md:grid-cols-3">
          <div
            class="p-6 transition-transform rounded-lg shadow-lg bg-zinc-800 hover:scale-105"
          >
            <h3 class="mb-3 text-xl font-bold text-amber-400">每月作品展示</h3>
            <p class="mb-4">
              上传您的绢花作品，有机会被选为月度精选，并获得专属奖励。
            </p>
            <button
              class="px-4 py-2 text-white transition rounded-lg bg-amber-600 hover:bg-amber-500"
            >
              查看本月作品
            </button>
          </div>

          <div
            class="p-6 transition-transform rounded-lg shadow-lg bg-zinc-800 hover:scale-105"
          >
            <h3 class="mb-3 text-xl font-bold text-amber-400">线上工艺课堂</h3>
            <p class="mb-4">
              参与我们的线上课程，向绢花大师学习传统与创新技艺。
            </p>
            <button
              class="px-4 py-2 text-white transition rounded-lg bg-amber-600 hover:bg-amber-500"
            >
              查看课程安排
            </button>
          </div>

          <div
            class="p-6 transition-transform rounded-lg shadow-lg bg-zinc-800 hover:scale-105"
          >
            <h3 class="mb-3 text-xl font-bold text-amber-400">创意挑战赛</h3>
            <p class="mb-4">参与主题创作挑战，展示您的创意，赢取丰厚奖品。</p>
            <button
              class="px-4 py-2 text-white transition rounded-lg bg-amber-600 hover:bg-amber-500"
            >
              查看当前挑战
            </button>
          </div>
        </div>
      </div>
    </section>
    <!-- 定制区 -->
    <section
      id="ai-design-section"
      class="w-full py-10 bg-zinc-900 section-container"
      v-if="isCustomPage"
      style="
        background: linear-gradient(135deg, #2a241c, #4b4034 30%, #2a241c 70%);
      "
    >
      <div class="max-w-6xl px-4 mx-auto">
        <div class="mb-10 text-center">
          <h2 class="mb-6 text-4xl font-bold">设计您的专属绢花</h2>
          <p class="mb-4 text-lg">
            使用我们的AI工具，设计属于您自己的绢花饰品。
          </p>
        </div>

        <!-- AI设计工具区域 -->
        <div class="grid grid-cols-1 gap-8 md:grid-cols-2">
          <!-- 左侧：AI生成区 -->
          <div class="p-6 rounded-lg shadow-xl bg-zinc-800">
            <h3 class="mb-4 text-2xl font-bold text-amber-400">AI绢花生成器</h3>

            <!-- 设计选项 -->
            <div class="mb-6">
              <div class="mb-4">
                <label class="block mb-2 text-sm font-medium">绢花类型</label>
                <select
                  v-model="designOptions.flowerType"
                  class="w-full p-2 border rounded-md bg-zinc-700 border-zinc-600"
                >
                  <option v-for="type in flowerTypes" :key="type" :value="type">
                    {{ type }}
                  </option>
                </select>
              </div>

              <div class="mb-4">
                <label class="block mb-2 text-sm font-medium">颜色主题</label>
                <div class="flex flex-wrap gap-2">
                  <div
                    v-for="color in colorThemes"
                    :key="color.name"
                    :style="{ backgroundColor: color.value }"
                    class="w-8 h-8 border-2 rounded-full cursor-pointer"
                    :class="{
                      'border-amber-400':
                        designOptions.colorTheme === color.name,
                      'border-transparent':
                        designOptions.colorTheme !== color.name,
                    }"
                    @click="designOptions.colorTheme = color.name"
                  ></div>
                </div>
              </div>

              <div class="mb-4">
                <label class="block mb-2 text-sm font-medium">风格</label>
                <div class="flex flex-wrap gap-2">
                  <button
                    v-for="style in designStyles"
                    :key="style"
                    @click="designOptions.style = style"
                    class="px-3 py-1 text-sm rounded-full"
                    :class="
                      designOptions.style === style
                        ? 'bg-amber-600 text-white'
                        : 'bg-zinc-700 text-gray-300 hover:bg-zinc-600'
                    "
                  >
                    {{ style }}
                  </button>
                </div>
              </div>

              <div class="mb-4">
                <label class="block mb-2 text-sm font-medium"
                  >描述您的想法 (可选)</label
                >
                <textarea
                  v-model="designOptions.description"
                  class="w-full h-20 p-2 border rounded-md bg-zinc-700 border-zinc-600"
                  placeholder="描述您想要的绢花外观、用途或灵感来源..."
                ></textarea>
              </div>
            </div>

            <!-- 生成按钮 -->
            <button
              @click="generateDesign"
              class="w-full py-3 font-bold text-white transition rounded-lg shadow-lg bg-gradient-to-r from-amber-600 to-amber-800 hover:from-amber-500 hover:to-amber-700"
              :disabled="isGenerating"
            >
              <span v-if="isGenerating">
                <i class="mr-2 fas fa-spinner fa-spin"></i> 正在生成...
              </span>
              <span v-else>生成我的专属绢花设计</span>
            </button>
          </div>

          <!-- 右侧：结果展示区 -->
          <div class="flex flex-col p-6 rounded-lg shadow-xl bg-zinc-800">
            <h3 class="mb-4 text-2xl font-bold text-amber-400">设计预览</h3>

            <div
              v-if="isGenerating"
              class="flex items-center justify-center flex-grow"
            >
              <div class="text-center">
                <div
                  class="inline-block w-12 h-12 mb-4 border-t-2 border-b-2 rounded-full animate-spin border-amber-500"
                ></div>
                <p>AI正在为您创作独特设计...</p>
              </div>
            </div>

            <div v-else-if="generatedDesign" class="flex flex-col flex-grow">
              <div
                class="relative flex-grow overflow-hidden rounded-lg bg-zinc-900"
              >
                <img
                  :src="generatedDesign.imageUrl"
                  class="object-contain w-full h-full"
                  alt="生成的绢花设计"
                />
              </div>

              <div class="p-4 mt-4 rounded-lg bg-zinc-700">
                <h4 class="mb-2 font-bold text-amber-400">AI设计说明</h4>
                <p class="text-sm">{{ generatedDesign.description }}</p>
              </div>

              <div class="flex gap-3 mt-4">
                <button
                  class="flex-1 py-2 text-white transition rounded-lg bg-amber-600 hover:bg-amber-500"
                >
                  保存设计
                </button>
                <button
                  class="flex-1 py-2 text-white transition rounded-lg bg-zinc-700 hover:bg-zinc-600"
                >
                  调整设计
                </button>
                <button
                  class="flex-1 py-2 text-white transition rounded-lg bg-zinc-700 hover:bg-zinc-600"
                >
                  咨询定制
                </button>
              </div>
            </div>

            <div
              v-else
              class="flex items-center justify-center flex-grow rounded-lg bg-zinc-900"
            >
              <div class="p-6 text-center">
                <!-- 使用已有的图片替代不存在的flower-placeholder.svg -->
                <img
                  src="/images/rightsilk.jpg"
                  class="w-24 h-24 mx-auto mb-4 opacity-30"
                  alt="设计占位图"
                />
                <p class="text-gray-400">
                  选择您喜欢的选项，点击生成按钮创建专属设计
                </p>
              </div>
            </div>
          </div>
        </div>

        <!-- 历史设计展示 -->
        <div class="mt-12">
          <h3 class="mb-6 text-2xl font-bold text-center">社区优秀设计</h3>

          <div class="grid grid-cols-2 gap-4 sm:grid-cols-3 md:grid-cols-4">
            <!-- 使用已有的图片 -->
            <div
              v-for="(design, index) in communityDesigns"
              :key="index"
              class="overflow-hidden transition-transform rounded-lg shadow-lg bg-zinc-800 hover:scale-105"
            >
              <img
                :src="design.imageUrl"
                class="object-cover w-full aspect-square"
                :alt="design.name"
              />
              <div class="p-3">
                <h4 class="font-bold truncate text-amber-400">
                  {{ design.name }}
                </h4>
                <p class="text-xs text-gray-400">by {{ design.designer }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <!-- 页脚 -->
    <footer
      class="w-full py-5 text-center shadow-2xl"
      style="background: linear-gradient(180deg, #0a0a0a, #000000)"
    >
      <p class="text-sm text-gray-500">© 2025 一朵顷刻品牌官网. 保留所有权利。</p>
      <div class="mt-2">
        <a
          href="/privacy"
          class="text-blue-500 transition-all duration-300 ease-in-out hover:text-blue-400"
          >隐私政策</a
        >
        <span class="mx-2 text-gray-600">|</span>
        <a
          href="/terms"
          class="text-blue-500 transition-all duration-300 ease-in-out hover:text-blue-400"
          >服务条款</a
        >
      </div>
    </footer>
  </div>
</template>

<script>
import axios from "axios";

export default {
  data() {
    return {
      isHomePage: true,
      isProductPage: false,
      isCommunityPage: false,
      isCustomPage: false,
      // 合并products和newProducts为一个allProducts数组
      allProducts: [
        // 原来的products
        {
          name: "绢花项链",
          description: "经典而现代，让您时刻优雅。",
          image: "/images/necklace.jpg",
          link: "https://item.jd.com/1110592.html",
        },
        {
          name: "绢花耳环",
          description: "精致迷人，点亮时刻。",
          image: "/images/earrings.jpg",
          link: "https://detail.tmall.com/item.htm?id=605165654577",
        },
        {
          name: "绢花胸针",
          description: "艺术典雅，独特魅力。",
          image: "/images/brooch.jpg",
          link: "https://item.jd.com/2222222.html",
        },
        {
          name: "绢花戒指",
          description: "精致小巧，优雅迷人。",
          image: "/images/flower-ring.jpg",
          link: "https://item.jd.com/4444444.html",
        },
        {
          name: "绢花手链",
          description: "独特设计，佩戴舒适。",
          image: "/images/bracelet.jpg",
          link: "https://item.jd.com/5555555.html",
        },
        {
          name: "绢花别针",
          description: "精美设计，细腻工艺。",
          image: "/images/pin.jpg",
          link: "https://item.jd.com/6666666.html",
        },
        // 原来的newProducts
        {
          name: "绢花发簪",
          description: "古典雅致，点缀发间风情。",
          image: "/images/rightsilk.jpg",
          link: "https://item.jd.com/7777777.html",
        },
        {
          name: "绢花耳坠",
          description: "灵动飘逸，演绎东方美学。",
          image: "/images/ear-drop.jpg",
          link: "https://detail.tmall.com/item.htm?id=7071777777",
        },
        {
          name: "绢花胸饰",
          description: "立体造型，彰显独特品味。",
          image: "/images/brooch-new.jpg",
          link: "https://item.jd.com/8888888.html",
        },
        {
          name: "绢花手镯",
          description: "柔美缠绕，腕间艺术绽放。",
          image: "/images/bracelet-new.jpg",
          link: "https://item.jd.com/9999999.html",
        },
        {
          name: "绢花摆件",
          description: "居家装饰，传承文化之美。",
          image: "/images/decoration.jpg",
          link: "https://item.jd.com/10101010.html",
        },
        {
          name: "绢花香囊",
          description: "古法熏香，承载美好祈愿。",
          image: "/images/sachet.jpg",
          link: "https://item.jd.com/12121212.html",
        },
      ],
      // AI设计工具相关
      designOptions: {
        flowerType: "牡丹",
        colorTheme: "传统红",
        style: "古典",
        description: "",
      },
      flowerTypes: [
        "牡丹",
        "莲花",
        "梅花",
        "兰花",
        "菊花",
        "玫瑰",
        "百合",
        "桃花",
      ],
      colorThemes: [
        { name: "传统红", value: "#cc0000" },
        { name: "典雅紫", value: "#8a2be2" },
        { name: "祥和黄", value: "#ffd700" },
        { name: "清新绿", value: "#228b22" },
        { name: "沉稳蓝", value: "#4169e1" },
        { name: "高贵金", value: "#d4af37" },
        { name: "纯净白", value: "#f5f5f5" },
        { name: "神秘黑", value: "#2c2c2c" },
      ],
      designStyles: [
        "古典",
        "现代",
        "简约",
        "奢华",
        "民族",
        "复古",
        "自然",
        "艺术",
      ],
      isGenerating: false,
      generatedDesign: null,

      // 社区设计展示 - 使用已有的图片
      communityDesigns: [
        {
          id: 1,
          name: "金丝牡丹胸针",
          designer: "花间一壶酒",
          imageUrl: "/images/brooch.jpg",
        },
        {
          id: 2,
          name: "紫韵兰花发簪",
          designer: "墨香书生",
          imageUrl: "/images/rightsilk.jpg",
        },
        {
          id: 3,
          name: "流苏梅花耳坠",
          designer: "清风明月",
          imageUrl: "/images/earrings.jpg",
        },
        {
          id: 4,
          name: "翠玉莲花项链",
          designer: "江南烟雨",
          imageUrl: "/images/necklace.jpg",
        },
        {
          id: 5,
          name: "红绡菊花手链",
          designer: "山水有情",
          imageUrl: "/images/bracelet.jpg",
        },
        {
          id: 6,
          name: "金丝玫瑰戒指",
          designer: "云端漫步",
          imageUrl: "/images/flower-ring.jpg",
        },
        {
          id: 7,
          name: "青玉百合摆件",
          designer: "竹影清风",
          imageUrl: "/images/decoration.jpg",
        },
        {
          id: 8,
          name: "锦绣桃花香囊",
          designer: "月下独酌",
          imageUrl: "/images/sachet.jpg",
        },
      ],
    };
  },
  methods: {
    // 生成AI设计
    async generateDesign() {
      this.isGenerating = true;

      try {
        // 构建提示词
        const prompt = `一朵精美的${this.designOptions.colorTheme}色${this.designOptions.flowerType}绢花，${this.designOptions.style}风格，${this.designOptions.description}`;

        // 模拟API调用，实际项目中替换为真实API
        // 由于这是演示，我们使用已有图片模拟生成结果
        await new Promise((resolve) => setTimeout(resolve, 2000)); // 模拟加载时间

        // 随机选择一张已有图片作为"生成"结果
        const availableImages = [
          "/images/rightsilk.jpg",
          "/images/necklace.jpg",
          "/images/earrings.jpg",
          "/images/brooch.jpg",
          "/images/flower-ring.jpg",
          "/images/bracelet.jpg",
          "/images/pin.jpg",
        ];

        const randomImage =
          availableImages[Math.floor(Math.random() * availableImages.length)];

        // 设置生成结果
        this.generatedDesign = {
          imageUrl: randomImage,
          description: `这是一款${this.designOptions.style}风格的${
            this.designOptions.colorTheme
          }色${
            this.designOptions.flowerType
          }绢花设计。${this.getRandomDescription()}`,
        };
      } catch (error) {
        console.error("生成设计时出错:", error);

        // 使用备用图像
        this.generatedDesign = {
          imageUrl: "/images/rightsilk.jpg",
          description: `由于当前请求量较大，我们提供了一个${this.designOptions.style}风格的${this.designOptions.flowerType}设计参考。您可以稍后再试或联系我们的设计师进行定制。`,
        };
      } finally {
        this.isGenerating = false;
      }
    },

    // 获取随机描述文本
    getRandomDescription() {
      const descriptions = [
        "精细的丝绸材质展现出柔美质感，每一片花瓣都栩栩如生。",
        "采用传统工艺与现代审美相结合，既保留了传统绢花的精髓，又融入了现代设计元素。",
        "每一处细节都经过精心打磨，展现出匠人的用心与专注。",
        "色彩层次丰富，在不同光线下呈现出变幻的美感。",
        "可作为胸针、发饰或装饰品，多种佩戴方式满足不同场合需求。",
        "灵感源自自然之美，将花朵的灵动与丝绸的柔美完美融合。",
      ];
      return descriptions[Math.floor(Math.random() * descriptions.length)];
    },
  },
};
</script>

<style>
/* 可以添加一些全局样式 */
@import url("https://fonts.googleapis.com/css2?family=Noto+Serif+SC:wght@400;700&display=swap");

.font-microsoftYaHei {
  font-family: "Microsoft YaHei", "Noto Serif SC", serif;
}

/* 自定义滚动条样式 */
::-webkit-scrollbar {
  width: 8px;
}

::-webkit-scrollbar-track {
  background: #2d2d2d;
}

::-webkit-scrollbar-thumb {
  background: #555;
  border-radius: 4px;
}

::-webkit-scrollbar-thumb:hover {
  background: #777;
}

/* 添加一些动画效果 */
@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

.fade-in {
  animation: fadeIn 0.5s ease-in-out;
}

/* 响应式调整 */
@media (max-width: 768px) {
  .forumHeight {
    height: 600px;
  }
}

.section-container {
  padding-top: 80px;
}

#ai-design-section,
#community-section {
  padding-top: 100px;
  margin-top: -20px;
}

html {
  scroll-padding-top: 80px;
}
</style>
