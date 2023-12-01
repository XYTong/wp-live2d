# Live2d compatible with wordpress page
基于[AzurLaneL2DViewer](https://github.com/Yukariin/AzurLaneL2DViewer)
Based on [AzurLaneL2DViewer](https://github.com/Yukariin/AzurLaneL2DViewer)
and fixed some small bugs
## Usage
1. Clone this repo
    Clone本仓库
2. Add the following content to your header.php:
    修改路径并添加如下内容到你的header文件(html或php)
    ```html
    <!-- Canvas -->
    <div class="Canvas left"></div>
    <script src="js/jquery.min.js"></script>
    <script src="js/bootstrap.min.js"></script>
    
    <!-- Live2DCubismCore -->
    <script src="js/live2dcubismcore.min.js"></script>

    <!-- Include Pixi. -->
    <script src="js/pixi.min.js"></script>

    <!-- Include Cubism Components. -->
    <script src="js/live2dcubismframework.js"></script>
    <script src="js/live2dcubismpixi.js"></script>

    <!-- User's Script -->
    <script src="js/charData.js"></script>
    <script src="https://cdn.jsdelivr.net/gh/litstronger/live2d-moc3@master/js/l2d.js"></script>
    <script src="js/main.js"></script>
    ```
3. Modify and add the following content to your footer.php. Basepath is your url of live2d root directory:
    修改并添加如下内容到你的footer.php或.html
    ```html
    <div class="Canvas"  id="L2dCanvas"></div>
	<script>
		var config = {
			width: window.innerWidth/3,
			height: window.innerHeight/3,
			left: '-150px',
			bottom: '50px',
			basePath: 'your live2d root path of url',
			role: 'wuqi_2',
			opacity: 1,
			mobile: false
		}
		var v = new Viewer(config);
	</script>
    ```
4. See example in `index.html`
