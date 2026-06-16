---
# Практическое задание 28

## ЭФМО-02-25 

## Алиев Каяхан Командар оглы
---
# Тема работы
Сравнение REST и GraphQL: разработка одного и того же функционала двумя способами

## Цели занятия
Понять сильные и слабые стороны REST и GraphQL на практике: как меняется клиентский сценарий, сколько запросов нужно, как устроены ошибки, что легче документировать и кэшировать.

## Коды статуса:
-	200 OK — успешный ответ
-	201 Created — ресурс создан
-	204 No Content — успешно, без тела
-	400 Bad Request — неверные данные
-	404 Not Found — ресурс не найден
-	422 Unprocessable Entity — некорректные данные по смыслу
-	500 Internal Server Error — внутренняя ошибка

# Примечания по конфигурации и требования

Для запуска требуется:

Go: версия 1.25.1

<img width="841" height="232" alt="Установка Git и Go" src="https://github.com/user-attachments/assets/8e01d831-5a7f-4376-8348-9052b240aec9" />


# Команды запуска/сборки
## 1) Клонировать данный репозиторий в удобную для вас папку:
```Powershell
git clone https://github.com/kayahan81/pz28
```
## 2) Перейти в папку pz19:
```Powershell
cd pz28
```
## 3) Загрузка зависимостей:
```Powershell
go mod tidy
```
## 4) Команда запуска
В первом окне
```Powershell
go run
```

# Проверка работоспособности
## Получить токен 
```Powershell
curl -s -X POST http://localhost:8081/v1/auth/login `
  -H "Content-Type: application/json" `
  -d '{\"username\":\"student\",\"password\":\"student\"}'
```
## Получить список задач
```Powershell
curl -s http://localhost:8082/v1/tasks `
  -H "Authorization: Bearer demo-token"
```
