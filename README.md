- š Hi, Iām @ishikawa0121
- š Iām interested in ...
- š± Iām currently learning ...
- šļø Iām looking to collaborate on ...
- š« How to reach me ...

<!---
ishikawa0121/ishikawa0121 is a āØ special āØ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
import cv2
import numpy as np
import matplotlib.pyplot as plt

#ćć¹ćć°ć©ć č”Øē¤ŗ
def histgram(image,filename):
    histR = cv2.calcHist([image],[0,], None,[256,],[0,255,])
    histG = cv2.calcHist([image],[1,], None,[256,],[0,255,])
    histB = cv2.calcHist([image],[2,], None,[256,],[0,255,])


    plt.title("Histgram")
    plt.plot(histR,c='red',label='red')
    plt.plot(histG,c='green',label='green')
    plt.plot(histB,c='blue',label='blue')
    plt.grid()
    plt.show()
    
def main():
    image = cv2.imread('001.jpg',cv2.IMREAD_COLOR)
    if image is None:
        print('ćć”ć¤ć«ćććć¾ćć')
        exit(0) 

    #å„åē»åč”Øē¤ŗ      
    cv2.imshow('Original Image',image)
    cv2.waitKey()

    alpha = 1.0  #ć³ć³ćć©ć¹ćé ē®
    beta = 50    #ęććé ē®

    #ęććć»ć³ć³ćć©ć¹ćęä½
    res_image = cv2.convertScaleAbs(image,alpha = alpha,beta = beta)

    #ē»åč”Øē¤ŗ
    capt = 'New Image alpha=%.1f beta=%.1f'%(alpha,beta)
    cv2.imshow(capt, res_image)
    cv2.waitKey()

    #ćć¹ćć°ć©ć č”Øē¤ŗ
    histgram(res_image, capt + '.bmp')



if __name__ == '__main__':
    main()
--->
