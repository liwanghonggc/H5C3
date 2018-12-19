1、HTML5支持
   支持:所有的主流浏览器都支持h5.(chrome,firefox,safari...).IE9及以上支持h5(有选择的支持,
        并不会全部支持),但是ie8及以下不支持h5.

   改变了用户与文档的交互方式:多媒体:video audio canvas

   增加了其它的新特性:语义特性,本地存储特性,网页多媒体,二维三维,特效(过渡,动画)

   相对于h4:
   	1.进步:抛弃了一些不合理不常用的标记和属性
   	2.新增了一些标记和属性--表单
   	3.从代码角度而言,h5的网页结构代码更简洁

2、H5表单新增的一些标签
   电话 type = "tel";
   网址 url
   数量 number
   商品名称 search
   范围 range
   颜色 color
   时间 time
   日期 date
   日期时间 datetime(safari支持) datetime-local

3、H5表单新增的事件
   1) oninput:监听当前指定元素内容的改变,只要内容改变(添加内容、删除内容),就会触发这个事件
   2) onkeyup:键盘弹起的时候触发,每一个键的弹起都会触发一次
   3) oninvalid:当验证不通过时触发

4、H5新增的其他一些标签
   1) 进度条progress
   2) 度量器,衡量当前的进度值meter

5、H5多媒体标签
   1) audio
      <audio src="../mp3/aa.mp3" controls autoplay></audio>
      src:播放文件的路径
      controls:音频播放器的控制器面板
      autoplay:自动播放
      loop:循环播放

   2) video
      <video src="../mp3/mp4.mp4" poster="../images/l1.jpg" controls  height="600"></video>
      src:播放文件的路径
      controls:音频播放器的控制器面板
      autoplay:自动播放
      loop:循环播放
      poster:指定视频还没有完全下载完毕,或者用户没有点击播放前显示的封面.默认显示当前视频文件的第一副图像
      width:视频的宽度
      height:视频的高度

      source:因为不同的浏览器所支持的视频格式不一样,为了保证用户能够看到视频,我们可以提供多个视频文件让浏览器自动选择
      <video controls>
          <!--视频源，可以有多个源-->
          <source src="../mp3/flv.flv" type="video/flv">
          <source src="../mp3/mp4.mp4" type="video/mp4">
      </video>


