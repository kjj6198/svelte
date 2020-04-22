<script>
	import { Blurb, Hero, Section } from '@sveltejs/site-kit';
	import Contributors from './_components/Contributors.svelte';
	import Example from './_components/Example.svelte';
	import WhosUsingSvelte from './_components/WhosUsingSvelte.svelte';
	// import Lazy from '../components/Lazy.svelte';

	// TODO this causes a Sapper CSS bug...
	// function loadReplWidget() {
	// 	console.log('lazy loading');
	// 	return import('../components/Repl/ReplWidget.svelte').then(mod => mod.default);
	// }
</script>

<style>
	/* darken text for accessibility */
	/* TODO does this belong elsewhere? */
	:global(.back-light) {
		--text: hsl(36, 3%, 44%);
	}

	.examples {
		background: var(--second);
		color: white;
		overflow: hidden;
	}
</style>

<svelte:head>
	<title>Svelte • Cybernetically enhanced web apps</title>

	<meta name="twitter:title" content="Svelte">
	<meta name="twitter:description" content="Cybernetically enhanced web apps">
	<meta name="Description" content="Cybernetically enhanced web apps">
</svelte:head>

<Hero
	title="Svelte"
	tagline="Cybernetically enhanced web apps"
	outline="svelte-logo-outline.svg"
	logotype="svelte-logotype.svg"
/>

<Blurb>
	<a href="blog/write-less-code" slot="one">
		<h2>寫更少的程式碼</h2>
		<p>用你已經知道的語言 HTML, CSS 以及 JavaScript 建立元件</p>

		<span class="learn-more">看更多</span>
	</a>

	<a href="blog/virtual-dom-is-pure-overhead" slot="two">
		<h2>沒有 Virual DOM</h2>
		<p>Svelte 會將你的程式碼編譯成小型的、無框架的 JS 程式碼，App 啟動將會非常快速</p>

		<span class="learn-more">看更多</span>
	</a>

	<a href="blog/svelte-3-rethinking-reactivity" slot="three">
		<h2>真正的響應式</h2>
		<p>不需要複雜的狀態管理套件 — Svelte 本身已經實作 reactivity 到 JavaScript</p>

		<span class="learn-more">看更多</span>
	</a>

	<div class="description" slot="what">
		<p>Svelte 用一個全新的方法構築你的使用者介面。當傳統的框架像是 React 及 Vue 做非常多的工作在<em>瀏覽器</em>當中，Svelte 在你打包 App 時將工作搬到<em>編譯階段</em>處理</p>

		<p>Svelte 不使用像是虛擬 DOM 的 diff 機制，而是在你的 App 狀態有變化時精準地更新 DOM</p>

		<p><a href="blog/svelte-3-rethinking-reactivity">閱讀簡介文章</a>學習更多</p>
	</div>

	<div style="grid-area: start; display: flex; flex-direction: column; min-width: 0" slot="how">
		<pre class="language-bash" style="margin: 0 0 1em 0; min-width: 0; min-height: 0">
npx degit <a href="https://github.com/sveltejs/template" style="user-select: initial;">sveltejs/template</a> my-svelte-project
<span class="token comment"># or download and extract <a href="https://github.com/sveltejs/template/archive/master.zip">this .zip file</a></span>
cd my-svelte-project

npm install
npm run dev
		</pre>

		<p style="flex: 1">看看 <a href="blog/the-easiest-way-to-get-started">快速導覽</a>獲得更多資訊</p>

		<p class="cta"><a rel="prefetch" href="tutorial">學習 Svelte</a></p>
	</div>
</Blurb>

<div class="examples">
	<Example id="hello-world">
		<p>Svelte 元件建構在 HTML 之上，只要加入資料就好。</p>
	</Example>

	<Example id="nested-components">
		<p>CSS 預設只在元件作用域當中生效。不再有更多樣式衝突或是優先級問題，或者你也可以使用<a href="/blog/svelte-css-in-js">你最喜歡的 CSS-in-JS 套件</a>。</p>
	</Example>

	<Example id="reactive-assignments">
		<p>透過賦值給區域變數就可以觸發高效率且精細的更新。剩下的事交給編譯器處理。</p>
	</Example>

	<Example id="svg-transitions">
		<p>使用內建於框架中，強大且性能優越的動畫引擎（transition engine）來構建漂亮的 UI。</p>
	</Example>
</div>

<Section>
	<h3>誰在用 Svelte？</h3>

	<WhosUsingSvelte/>
</Section>

<Section>
	<h3>貢獻者們</h3>

	<p>Svelte 是免費且開源的軟體，大量貢獻者的參與讓許多事情是可能的。<a href="https://github.com/sveltejs/svelte">加入我們！</a></p>

	<Contributors/>
</Section>
