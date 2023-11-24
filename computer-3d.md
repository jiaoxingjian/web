# computer / 3d
## freecad
- [ ] [FreeCAD 介紹](https://www.youtube.com/watch?v=uLRbzs51viY) 参考开发文档 [freecad python scripting](http://staff.ltam.lu/feljc/software/freecad/fc_scripting_summary.pdf)
- [ ] [I made a DUMMY ROBOTIC ARM from scratch！](https://www.youtube.com/watch?v=F29vrvUwqS4) 
- [ ] [作者介绍：   华为天才少年稚晖君 ](https://www.google.com.hk/search?q=%E7%A8%9A%E6%99%96%E5%90%9B&sourceid=chrome&ie=UTF-8)
- [ ] [“民用外骨骼”本田助步器试用，CES Asian上本田不务正业的产品【科技小巴|Tech Bus】](https://www.youtube.com/watch?v=LLSrIXKmE3k)
- [ ] [FreeCAD: Recording operations as a Python script and executing it from the command line](https://www.xsim.info/articles/FreeCAD/en-US/HowTo/Use-FreeCAD-on-command-line.html)

- https://iosoft.blog/2019/05/22/3d-design-python-freecad/

- https://subscription.packtpub.com/book/iot-&-hardware/9781849518864/1/ch01lvl1sec14/creating-3d-solids-with-python-(become-an-expert)

  ```
  plate = Part.makeBox(40,40,5,Vector(-20,-20,0))
  hole1= Part.makeCylinder(1.5,5,Vector(-15,-15,0))
  hole2= Part.makeCylinder(1.5,5,Vector(-15,15,0))
  hole3= Part.makeCylinder(1.5,5,Vector(15,15,0))
  hole4= Part.makeCylinder(1.5,5,Vector(15,-15,0))
  faceplate = plate.cut(hole1)
  faceplate = faceplate.cut(hole2)
  faceplate = faceplate.cut(hole3)
  faceplate = faceplate.cut(hole4)
  motorbody=Part.makeCylinder(17.5,60,Vector(0,0,5))
  shaft = Part.makeCylinder(3.175,15,Vector(0,0,-15))
  servo = motorbody.fuse(faceplate)
  servo = servo.fuse(shaft)
  servo.translate(Vector(-20,-20,0))
  servo.rotate(Vector(0,0,0),Vector(0,1,0),-90)
  Part.show(servo)
  ```

  

## 3d 打印服务

- [ ] [3D Print Without Using a 3D Printer By Using Shapeways!](https://www.youtube.com/watch?v=3JzsYcUU4Gc&pp=ygUPM2QgcHJpbnQgb25saW5l)
- [ ] [Online 3D Printing Service How it Works](https://www.youtube.com/watch?v=pcQzT4c5QcM&pp=ygUPM2QgcHJpbnQgb25saW5l)
- [ ] [Why My 3D Printing Business Failed, and How to Prevent it for Yours #3dprinting](https://www.youtube.com/watch?v=axFe2CxvQ0Y&pp=ygUPM2QgcHJpbnQgb25saW5l)



## 3d /cnc 木工

- [ ] [DIY必備工具，家用CNC機器讓你省錢又省心!](https://www.youtube.com/watch?v=K-e9IXQS3c8&t=929s&pp=ygUJY25j5pyo5bel)
- [ ] [木工教學 簡易CNC貓櫃初級班【超認真少年】How to Choose PVC, melamine, PP](https://www.youtube.com/watch?v=aoE5hlb9tXA&pp=ygUJY25j5pyo5bel)



## 3d 眼镜

- [ ] [Design eyeglasses or sunglasses by CAD](https://www.youtube.com/watch?v=YFdFM1BtKuw&pp=ygUPZnJlZWNhZCBnbGFzc2Vz)

- [ ] [I made a DUMMY ROBOTIC ARM from scratch！](https://www.youtube.com/watch?v=F29vrvUwqS4) http://www.baidu.com)

  

## 炒菜机

- [ ] [自動炒食機2013 營業版-炒青菜](https://www.youtube.com/watch?v=QH93mff6uLo&list=PLwEF1U7kKqZaTGYbGkVXDsS38H2mA0A5Z&index=1&t=169s)



## 音箱

- [ ] [How Speakers Make Sound](https://www.youtube.com/watch?v=RxdFP31QYAg&pp=ygUMM2Qgc291bmQgYm94)
- [ ] [Building EXCEPTIONAL speakers using MODERN TECHNIQUES](https://www.youtube.com/watch?v=XEspOD1NHr0&pp=ygUMM2Qgc291bmQgYm94)
- [ ] [Dolby Audio - 7.1 Surround Test Demo](https://www.youtube.com/watch?v=xCbLLge0tOE&pp=ygUMM2Qgc291bmQgYm94)