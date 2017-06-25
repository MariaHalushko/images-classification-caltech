# FAQ

* Зачем смотреть на данные:
  * Классы не равномерно распределены
  * Изображения различного размера
  * Colored and gray-style images
* Не влазит в память:
  * Можно ужать через PCA
  * Batch processing решит эту проблему(когда появятся сетки)
* А что все-же делать с неравномерностью классов:
  * Аугментируем недастоющие классы
  * Используем взешанную матрицу ошибки
  * Subsampling из большего класса
  * вообще есть paper - [Survey of resampling techniques for improving classification performance in unbalanced datasets](https://arxiv.org/pdf/1608.06048.pdf)
* Некоторые картинки graystyle:
  * Пока что самый простой вариант размножить изображение в 3 раза, что бы было 3 канала
* Иногда в выборке попадаются папки не с изображеними:
  * Да, такие папки есть - они начинаются на `.`. Просто проверяйте `if not f_name.startswith('.'); continue`
  * Еще попадаются внутри не изображения - проверяйте как `if not f_name.endswith('.jpg'); continue`