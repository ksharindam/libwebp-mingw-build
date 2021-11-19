# build libwebp under mingw32
Unofficial build and makefiles of libwebp


I am using mingw32 build of Qt4 for windows in one of my program (PhotoQuick).  
I wanted to ship webp image format plugin. But, precompiled libwebp is not available for mingw32. Also, there is no instructions to build libwebp using mingw32.  
So, after trying hard, I created some custom makefiles and successfully built libwebp.  

You can download precompiled version in the release page.  
Or you can build by yourself using these makefiles.  

## Build
1. Download libwebp source code from original website.  
2. Extract source code.  
3. copy src/ directory from this repo, paste over the src/ directory of libwebp source code.  
4. Open commandline inside libwebp/src directory.  
5. Run these commands  
```
mkdir build  
make -j4  
```
webp.dll and libwebp.a will be created inside src/ directory.  
All the header files are inside src/webp directory.  
