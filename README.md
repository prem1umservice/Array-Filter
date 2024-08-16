### Блок-схема

 graph LR
    A[Ввод массива строк] --> B{Длина строки <= 3?}
    B -- Да --> C[Увеличить new_array_size]
    B -- Нет --> D[Перейти к следующей строке]
    C --> B
    D --> B
    B -- Нет строк --> E[Создать new_array размером new_array_size]
    E --> F[i = 0]
    F --> G{Длина строки <= 3?}
    G -- Да --> H[Сохранить строку в new_array[i]]
    G -- Нет --> I[Перейти к следующей строке]
    H --> J[i = i + 1]
    J --> F
    I --> F
    F -- Нет строк --> K[Вывод new_array]
 


### Код

```python
def create_new_array(array):
  """
  Создает новый массив, содержащий только строки длиной не более 3 символов.

  Args:
    array: Исходный массив строк.

  Returns:
    Новый массив, содержащий строки длиной не более 3 символов.
  """
  new_array_size = 0
  for string in array:
    if len(string) <= 3:
      new_array_size += 1

  new_array = [""] * new_array_size
  i = 0
  for string in array:
    if len(string) <= 3:
      new_array[i] = string
      i += 1

  return new_array

if __name__ == "__main__":
  # Исходный массив строк
  array = ["Hello", "2", "world", ":-)"]

  # Формирование нового массива
  new_array = create_new_array(array)

  # Вывод результата
  print(f"Новый массив: {new_array}")```
