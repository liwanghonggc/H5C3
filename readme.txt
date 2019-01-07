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

6、H5的dom操作
   1) querySelector:获取单个元素,如果获取的元素不止一个,那么只会返回满足条件的第一个元素
                    参数要求:如果是类选择器,必须添加. 如果是id选择器,必须添加#,否则当成标签处理

   2) querySelectorAll获取满足条件的所有元素--数组

7、H5自定义属性
   <p data-school-name="itcast">传智播客</p>

   var p = document.querySelector("p");
   var value = p.dataset["data-school-name"];

8、网络状态改变事件
   1) ononline:网络连通的时候触发这个事件
      window.addEventListener("online", function(){
              alert("网络连通了");
      });
   2) onoffline:网络断开时触发

9、全屏API
   全屏操作的主要方法和属性
   1) requestFullScreen()  开启全屏显示,不同浏览器需要添加不同的前缀
                           chrome:webkit   firefox:moz   ie:ms   opera:o

                           全屏操作
                           document.querySelector("#full").onclick=function(){

                               /*div.requestFullScreen();*/
                               /*div.webkitRequestFullScreen();*/
                               /*div.mozRequestFullScreen();*/
                               /*使用能力测试添加不同浏览器下的前缀*/

                               if(div.requestFullScreen){
                                   div.requestFullScreen();
                               }
                               else if(div.webkitRequestFullScreen){
                                   div.webkitRequestFullScreen();
                               }
                               else if(div.mozRequestFullScreen){
                                   div.mozRequestFullScreen();
                               }
                               else if(div.msRequestFullScreen){
                                   div.msRequestFullScreen();
                               }
                           }

   2) cancelFullScreen()   退出全屏显示,也添加前缀,在不同的浏览器下退出全屏只能使用document来实现

                               退出全屏
                               document.querySelector("#cancelFull").onclick=function(){
                                   if(document.cancelFullScreen){
                                       document.cancelFullScreen();
                                   }
                                   else if(document.webkitCancelFullScreen){
                                       document.webkitCancelFullScreen();
                                   }
                                   else if(document.mozCancelFullScreen){
                                       document.mozCancelFullScreen();
                                   }
                                   else if(document.msCancelFullScreen){
                                       document.msCancelFullScreen();
                                   }
                               }

   3) fullScreenElement    是否是全屏状态,也只能使用document进行判断


10、文件读取接口,文件读取预览效果
    FileReader接口,读取文件内容,见01.文件读取FileReader.html

11、拖拽接口,常见拖拽效果
    在h5中,如果想拖拽元素,就必须为元素添加draggable="true". 图片和超链接默认就可以拖拽,见04.HTML5-拖拽接口的使用.html、05.HTML5-拖拽接口的使用-通用.html

12、地理定位接口,获取用户位置信息
    见案例06、07

13、web存储接口,实现数据的读写

14、应用缓存接口

15、多媒体接口,实现自定义播放器






























