- 👋 Hi, I’m @ishikawa0121
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
ishikawa0121/ishikawa0121 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
import cv2
import numpy as np
import matplotlib.pyplot as plt

#ヒストグラム表示
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
        print('ファイルがありません')
        exit(0) 

    #入力画像表示      
    cv2.imshow('Original Image',image)
    cv2.waitKey()

    alpha = 1.0  #コントラスト項目
    beta = 50    #明るさ項目

    #明るさ・コントラスト操作
    res_image = cv2.convertScaleAbs(image,alpha = alpha,beta = beta)

    #画像表示
    capt = 'New Image alpha=%.1f beta=%.1f'%(alpha,beta)
    cv2.imshow(capt, res_image)
    cv2.waitKey()

    #ヒストグラム表示
    histgram(res_image, capt + '.bmp')



if __name__ == '__main__':
    main()
--->
