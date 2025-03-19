---
title: Apps
date: "2025-03-19T23:46:37.121Z"
description: "Bible"
---

<p style="margin-top: 18px;">&emsp;</p>

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>视频播放页面</title>
    <link rel="stylesheet" href="./styles.css">
</head>

<body>
	<div class="container">
		<h1>Video Gallery</h1>
		
		<div class="video-grid">
			<!-- 第一行视频 -->
			<div class="video-card">
				<div class="video-wrapper">
					<video controls>
						<source src="https://uaomymsvd46s2yodz33sd42zfq7x2kknyx4xdmlo5dfxyp5cnqlq.arweave.net/oBzMMlUfPS1hw873IfNZLD99KU3F-XGxbujLfD-ibBc" type="video/mp4">
						您的浏览器不支持视频播放。
					</video>
					<a class="download-btn" title="下载视频">
						<svg viewBox="0 0 24 24" width="16" height="16">
							<path fill="currentColor" d="M19 9h-4V3H9v6H5l7 7 7-7zM5 18v2h14v-2H5z"/>
						</svg>
					</a>
				</div>
				<div class="video-info">
					<h3>Tense Oval Office argument between Zelensky, Trump and Vance</h3>
					<p>2025.3.1 北京时间凌晨0点, 川普、泽伦斯基、万斯白宫争吵。</p>
				</div>
			</div>

			<div class="video-card">
				<div class="video-wrapper">
					<video controls>
						<source src="./1.mp4" type="video/mp4">
						您的浏览器不支持视频播放。
					</video>
					<a class="download-btn" title="下载视频">
						<svg viewBox="0 0 24 24" width="16" height="16">
							<path fill="currentColor" d="M19 9h-4V3H9v6H5l7 7 7-7zM5 18v2h14v-2H5z"/>
						</svg>
					</a>
				</div>
				<div class="video-info">
					<h3>1400 Years of The Real History of Islam in 5 minutes</h3>
					<p>五分钟介绍伊斯兰1400年历史，由Brigitte Gabriel主讲，于 2018年5月19日发表。</p>
				</div>
			</div>

	</div>

	<script>
		// 添加下载处理函数
		function forceDownload(url) {
			// 从URL中提取文件名
			const fileName = url.split('/').pop();
			
			fetch(url)
				.then(response => response.blob())
				.then(blob => {
					const blobUrl = URL.createObjectURL(blob);
					const a = document.createElement('a');
					a.style.display = 'none';
					a.href = blobUrl;
					a.download = fileName;
					document.body.appendChild(a);
					a.click();
					
					setTimeout(() => {
						document.body.removeChild(a);
						URL.revokeObjectURL(blobUrl);
					}, 100);
				});
		}

		// 为所有下载按钮添加点击事件
		document.querySelectorAll('.download-btn').forEach(btn => {
			btn.addEventListener('click', (e) => {
				e.preventDefault();
				// 获取最近的video元素中的source标签的src属性
				const videoSource = btn.closest('.video-wrapper').querySelector('source');
				const videoUrl = videoSource.getAttribute('src');
				forceDownload(videoUrl);
			});
		});
	</script>
</body>


<p style="margin-bottom: 25px;">&emsp;</p>

