# Compress-the-photo-with-respect-to-aspect-ratio

from PIL import Image

image_path = '/home/pnvasko/PycharmProjects/pythonProject/hello.png'

# указываем фиксированный размер стороны
fixed_width = 200
img = Image.open(image_path)
# получаем процентное соотношение
# старой и новой ширины
width_percent = (fixed_width / float(img.size[0]))
# на основе предыдущего значения
# вычисляем новую высоту
height_size = int((float(img.size[0]) * float(width_percent)))
# меняем размер на полученные значения
new_image = img.resize((fixed_width, height_size))
new_image.show()
new_image.save('/home/pnvasko/PycharmProjects/pythonProject/hello.png')
