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

https://viewer.diagrams.net/?tags=%7B%7D&lightbox=1&highlight=0000ff&edit=_blank&layers=1&nav=1&title=%D0%94%D0%B8%D0%B0%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B0%20%D0%B1%D0%B5%D0%B7%20%D0%BD%D0%B0%D0%B7%D0%B2%D0%B0%D0%BD%D0%B8%D1%8F.drawio.png#R%3Cmxfile%3E%3Cdiagram%20name%3D%22%D0%A1%D1%82%D1%80%D0%B0%D0%BD%D0%B8%D1%86%D0%B0%20%E2%80%94%201%22%20id%3D%22fdrweQoV3BR5Cvi0iSNq%22%3E1Zhbk5sgGIZ%2FjZftiCjqZcxhe9OZzmxn2l66SqOzRjJITv31RUWFQHYzWXPYvWDl5RPleT9AYsHpav9E43X2naS4sBw73VtwZjn8DwH%2Br1YOrQJCN2yVJc1ToQ3Cc%2F4PC9EW6iZPcaUEMkIKlq9VMSFliROmaDGlZKeG%2FSWF%2BtR1vMSa8JzEha7%2BylOWtWrg%2BIP%2BDefLrHsyQGJ8q7gLFiOpsjglO0mCcwtOKSGsvVrtp7io6XVc2vsWJ1r7F6O4ZOfc4LQ3bONiI8ZmzWwrXFgzYAV2fR3NmxJKSltOpZI%2FxG4C3KYaNGXUKNOmdLrbeQmbVk%2Fojq30U4ugK%2FuunK5%2FoPbWv95E4GSHzqNdljP8vI6Tur7jiWjBqGKUvPaWcdjRFlOWc2MnRb4sucZIHadTFGDrcLyXJEH1CZMVZvTAQ0TrF0F2N%2BSHg4JWy6Tc4MTatBQpuex7GlzjF8I4s4nQbOJMQupLxkWC22XERmATCg5i%2BjuehspECo5AyjWTckSSDfnkdnkZSGnnKQF1OWv0SLSKW1yJ9cwUdi%2FuMFS4g46oBB4E6DrkPSP5ybvrRZ%2FBSLJjcSlqmpHVy6YyAjbZMAZ0qCY7CHTooSHde%2FEj1NG5y7sjrcm2WFGVhf30wtvacrekRo7C10VI5%2Bva10lq34y3y8r7MVEnutfVJSbwSvM8eGsv6vf8e4EBnvcuGde5Dpnw5N7TLljGHaifbe3e40sfUEfLZb849h9ZvJw3ZSj1ALvN%2F7zPrnslsvAHeVDzx0HudQzqTheyQ8cjTzZ0i%2Bt40Aw5pmxSnye4UJKSx0S4TDvlpSDJay3tc%2Fab1%2B2vnqj9ER1wMPQgNdXVus1%2Bi15FNjTBypcff48lZsonDk6VI4xOmOIiZvlWPdGY8DW38jHFBylgTfKSVRrdvv%2FzgINPB9zVgXufCLjhuPfgwD0dOPpEwPWj2U%2FKr8aFzr%2FrT1MHF2FHOnb%2FxthFzz9qYdjBA1%2FdwMXCP1jUdnixYfoJcREX1diOoVsYFjyEYcBH13XMcLIceU0Dp91y4UVu%2Bbpb4UO4dTS9kEii0cwyHEhvZ5bnX2RW8KhmHU%2BtD7rFq8MPz2348Ps9nP8H%3C%2Fdiagram%3E%3C%2Fmxfile%3E#%7B%22pageId%22%3A%22fdrweQoV3BR5Cvi0iSNq%22%7D
