## Вопрос 1

Поискал - на OVH с более-менее адекватными параметрами (10 ядер, 32 гб рам) 29к рублей в месяц. Аналогичная машина на яндекс облаке стоит 15к в месяц.

## Вопрос 2

1. Когда лучше контейнеры

Пример такой - мы хотим разворачивать приложение, состоящее из множества микросервисов. В таком случае контейнер будет быстрее разворачиваться и есть меньше ресурсов, чем ВМ. Более того, можно использовать всякие k8s для автоматизации развертывания

2. Когда лучше ВМ

Пример - мы хотим мало приложений, которые будет еще и требовать специфичные версию линукса. И допустим еще ядер будет мало. В таком случае контейнеры будут использовать общие ресурсы и для них еще будет тяжело настроить линукс под каждый конкретный контейнер. с виртуалками попроще - все изолировано и для каждой виртуалки можно настроить отдельно свои конфигурации

## Вопрос 3

Прерываемые вмки это такой вид вмок, которые могут прерываться в любой момент. Они дешевле непрерываемых, потому что бОльшая часть времени в яндекс облаке не имеет пиковые нагрузки, а как следствие имеет свободное железо (которое будет заниматься в пиковые нагрузки). Это свободное железо можно продавать подешевле с гарантией отключения когда это понадобится яндекс облаку.

Такие виртуалки полезны например для разработки. Можно на них собирать большие репозитории. 