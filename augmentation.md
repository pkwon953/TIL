# Augmentation

​	이미지를 학습하기 위해 data augmentation 과정을 거친다. 다양한 이미지에 대한 학습을 위해 필수적으로 이루어지는 과정이다.

## **Image preprocessing**

​	학습을 진행하기 전, 학습의 대상이 될 이미지를 분류하고 선별하는 작업을 의미한다.

> ```python
> img = tf.keras.preprocessing.image.load_img('image.jpg')
> data = tf.keras.preprocessing.image.img_to_array(img)
> ```
>
> 

​	이미지 객체에서 우선 data만 추출하는 작업이 이루어진다. 존재하는 데이터셋을 사용해 학습 데이터셋을 재구성한다.



# 기하변경

# flow

# next