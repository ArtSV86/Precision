**Отчёт о тестировании приложения "Precision"**

**Краткое описание**


Проведен тест формулы для расчета бонуса новым клиентам (double totalBonus = regularBonus + specialBonus), помимо стандартного бонуса (regularBonus = 0.3), добавляется специальный бонус (specialBonus = 0.6), воспроизведенной в java, где в качестве type=double:

```java
public class Main {
  public static void main(String[] args) {
    double regularBonus = 0.3;
    double specialBonus = 0.6;
    double totalBonus = regularBonus + specialBonus;
    System.out.println(totalBonus);
  }
}
```

Результат обработки:
```
TotalBonus = 0.8999999999999999
```


**Описание тестов**

Проводилось  функциональное, санитарное тестирование.

**Результаты**

[Bug-report](https://github.com/ArtSV86/Precision/issues/1)

   

**Общие рекомендации**

При расчете по следующей формуле получается требуемое 0,9:
```java
public class Main {
    public static void main(String[] args) {
        double regularBonus = 3;
        double specialBonus = 6;
        double totalBonus = (regularBonus + specialBonus)/100;
        System.out.println(totalBonus);
    }
}
```