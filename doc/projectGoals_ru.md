# Project Goals
## Зачем?

Для того, чтобы дать обычным людям больше возможностей при обмене информацией.

Cjdns позволяет решить множество проблем текущих сетей. При его использовании вы полностью обладаете своей инфраструктурой обмена информацией.

Кроме того, данный протокол позволяет решить проблему оптимального перераспределения трафика, не делая практически ничего.

Вот простой пример. Сколько у вас дома есть открытых Wi-Fi сетей?

Вероятно, не меньше двух. А теперь представьте, что они работают в Mesh режиме, динамически перенаправляя нагрузку и распределяя трафик.

Централизация власти проявляется в закрытии таких сайтов, как Wikileaks, и любых других — неугодных власти.

В цивилизованном, демократическом обществе каждый должен иметь свободу слова, а цензурироваться могут лишь очевидно-плохие вещи: детская порнография, мошенничество, спам. И конечно, решения о цензуре должно принимать общество, а не правительство.


## Как мы близки к финальной версии?

В данный момент работает тестовая сеть, в которой имеется от 500 до 1000 узлов.

Cjdns была протестирована на x86, amd64, ARMv5, ARMv7, MIPS, PowerPC32 и PowerPC64. Тестирование на различных Linux системах продолжается. 

Программное обеспечение работает стабильно, но мы не знаем, как поведут себя в реальном мире наши алгоритмы и протоколы. Пожалуйста, следите за обновлениями cjdns. С помощью тестирования мы сможем определить оптимальный набор алгоритмов и протоколов для использования в реальном мире.


## Ты можешь помочь!

Нам нужны добровольцы для тестирования по автоматической сборке cjdns на Apple OS X системе, если вы можете пожертвовать нам деньги для этого дела — напишите нам на почту.

Или же вы можете помочь нам, предоставив 24/7 shell доступ к компьютеру с системой OS X для проведения тестирования.

Всё это можно обсудить в нашем IRC канале.


## Анонимность

В отличии от TOR, I2P, и Freenet’a, cjdns планировалась не как анонимная есть. Она не использует случайную маршрутизацию, динамические маршруты и другие технологии для обеспечения анонимности.

Наоборот, cjdns использует самый оптимальный маршрут. Мы пошли на такой шаг, для обеспечения максимальной производительности.

С другой стороны, некий уровень анонимности всё же присутствует. Для того, чтобы определить ваше физическое положение на основе вашего cjdns адреса, потребуется сделать трассировку по IPv4 адресам от конечной ноды до вас, запросив информацию по проходящему трафику от операторов всех транзитных нод.


## Безопасность

Когда вы получаете информационный пакет из интернета, это означает, что он предназначен для вас, но никто не знает, модифицировался ли пакет по пути или же нет. Множество программ, которые взаимодействуют с интернетом, не проверяют неизменность пакета, а такие программно-аппаратные средства, как DPI, могут вносить значительные изменения в пакеты.

Cjdns гарантирует, что пакет по пути был не кем не модифицирован, что подтверждается криптографическими средствами, которые используются в этом протоколе.

Cjdns защищает информацию которая поступает к вам, от использования заведомо ложного маршрута, что позволяет полностью избежать атаки man-in-the-middle.


## Простота

Представьте себе такую компьютерную сеть, в которой всё, что нужно сделать инженеру — это подключить компьютер сетевым кабелем, а компьютер сам узнает, как найти других и сам сконфигурируется.

Это и есть основная цель cjdns. Конечно же, сетевые специалисты всё еще будут нужны для решения сложных технических вопросов, но большую часть решения проблем сможет взять на себя cjdns.


## Масштабируемость

С основе Cjdns лежат принципы одноранговой сети, таким образом, cjdns может масштабироваться бесконечно — нет большой нагрузки на какой-то определенный узел.
Cjdns использует распределенную хэш таблицу (DHT) для обмена маршрутами, это позволяет не иметь карту всей сети каждому узлу (не раздувать таблицу маршрутов).