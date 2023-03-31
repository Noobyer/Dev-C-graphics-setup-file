Instruction for adding graphics file in dev c++
***************************************************************************************************

1) Copy "graphics.h" and "winbgim.h" files to "include" folder of dev-cpp directory.
   Default location is ("C:\Program Files (x86)\dev-cpp\MinGW\include\")

2) Copy "libbgi.a" to file to "lib" folder of dev-cpp directory.
   Default location is ("C:\Program Files (x86)\dev-cpp\MinGW\lib\")

3) Open dev c++ and go to (Settings > Compiler > Linker Settings)

4) Link Libraries (left), Click on "Add" button, then click "Browse" and select the "libbbgi.a"
   file that you have copied in dev-cpp directory..
   Default location is (C:\Program Files (x86)\dev-cpp\MinGW\lib\libbgi.a)
   and then click "Open" button.

5) Other linker option (right), copy the text below and paste there
   -lbgi -lgdi32 -lcomdlg32 -luuid -loleaut32 -lole32

6) Click "OK"

Done...

NOTE that:
1) The graphics.h will work only in the program saved in ".cpp" format.

To check the graphics.h is working or not
*****************************************************************************************************
Create a new consol application in ".cpp" format and copy the codes given below, paste it in the
file you created and click "Build and Run" button or click "F9" key from your keyboard..

#include<graphics.h>
int main()
{
    int gd=DETECT,gm;
    initgraph(&gd,&gm,"");
    circle(200,200,100);
    getch();
}
