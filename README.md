
# 1.矢量切片部署 


## 1.1下载安装包

下载 http://10.8.9.165/index.php?dir=uploads/common/Packages/%E5%9C%B0%E5%9B%BE/ 路径下的 `Map-vectileServer.zip` 文件，打开可视化服务运维软件，在目标服务器下点击部署（图1-1-1）

图1-1-1
![image](image/1-1-1部署1.png) 

点击+，上传 `Map-vectileServer.zip` 软件包，服务自动部署启动，默认端口为8098

![image](image/1-1-1部署2.png)

## 1.2数据下载与放置目录详情

首先下载数据，下载 http://10.8.9.165/index.php?dir=uploads/common/Packages/%E5%9C%B0%E5%9B%BE/ 路径下的 `china.mbtiles` 文件 和  `world.mbtiles` 文件



数据放置在项目Map-vectileServer根目录下的data目录（目录示例：'C:\Program Files (x86)\Map-vectileServer\data\china.mbtiles','C:\Program Files (x86)\Map-vectileServer\data\world.mbtiles'），再点击启动服务，（图1-2-5）
 
图1-2-5

![image](image/1-2-5数据.png)















# 2.备注（非部署部分）

## 2.1.目前数据生产划分

   world.mbties（共12级）包含的图层数据： 

           国家边界world-country-line

           国家填充面world-country-polygon

           国家名称world_countryname_point

           中国省级边界china-province-line

           中国县边界china-xian-line

           中国县填充面china-xian-fill

           中国县名称china-xianname-point

           中国省会城市名称china-provincialcapital-point 

           中国省名称china-provincename-point

                                                       共计9个图层
   china.mbtiles（共14级）切片数据包含图层数据： 

           路网china_roads_line

           水系china_water_polygon

           土地使用china_landuse_polygon

           POI china_poi_point              
                   
                                                       共计4个图层
 
## 2.2.矢量切片调用

   对应的数据源:
 
      world.mbties数据源：世界/中国行政边界地名   

      style.sources.world.tiles[0] =  window.location.origin + "/map/mbview/world.mbtiles/{z}/{x}/{y}.pbf"

      china.mbtiles数据源：中国路网/poi/用地/水系 

      style.sources.china.tiles[0] =  window.location.origin + "/map/mbview/china.mbtiles/{z}/{x}/{y}.pbf"

 
   
 

 

 