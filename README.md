# GLSurfaceViewEGL14
使用android.opengl的包替换了 javax.microedition.khronos.egl包。

javax.microedition.khronos.egl包已经过时了，缺少很多扩展。
例如做视频录制时，视频又是基于GLSurfaceView的，如果要录制这个surface，缺少特性就不方便。

另外 做共享 opengl context时，如果有些部分是基于GLSurfaceView的，有的是自己写的EGL初始化的。
那么EGLContext会属于不同的类型。无法共享。基于这个GLSurfaceViewEGL14的就可以解决。
