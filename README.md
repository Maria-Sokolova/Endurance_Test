# Endurance_Test

# задача 1

Дано: Safe Browsing API

Необходимо: 

Получить информацию об актуальных списках Safe Browsing, хранящихся на серверах Яндекса.

Проверить хотя бы для двух URL содержатся ли они в списках Safe Browsing.

Решение:

Заходим на сайт https://yandex.ru/dev/safebrowsing/doc/quickstart/concepts/lookup.html  и во вкладке “Lookup. Проверка по URL” берем нужную информацию о запросе и вставляем в Postman.

Идем во вкладку  “Доступ к API” , далее переходим в “Кабинете разработчика”  и находим ключ

 Key #1
40d9595f-997b-4b27-ad1e-a1ee63461dfd 

вставляем его в Postman и выполняем запросы на получение информации и проверку для двух URL содержатся ли они в списках Safe Browsing 

Результат: 

[Uploading SafeBrowsing.postman_col{
	"info": {
		"_postman_id": "bb2e5b2b-706d-4073-bfb1-4d1ac25fe9c9",
		"name": "SafeBrowsing",
		"schema": "https://schema.getpostman.com/json/collection/v2.1.0/collection.json",
		"_exporter_id": "25548534",
		"_collection_link": "https://cloudy-station-174388.postman.co/workspace/Safe-Browsing~ca829872-6124-4c85-849c-89924b4846c2/collection/25548534-bb2e5b2b-706d-4073-bfb1-4d1ac25fe9c9?action=share&source=collection_link&creator=25548534"
	},
	"item": [
		{
			"name": "получение списка",
			"request": {
				"method": "GET",
				"header": [
					{
						"key": "Cookie",
						"value": "token_global={{token_global}}",
						"type": "text"
					}
				],
				"url": {
					"raw": "{{baseURL}}",
					"host": [
						"{{baseURL}}"
					]
				}
			},
			"response": []
		},
		{
			"name": "проверкаURL",
			"request": {
				"method": "POST",
				"header": [
					{
						"key": "Cookie",
						"value": "token_global={{token_global}}",
						"type": "text"
					}
				],
				"body": {
					"mode": "raw",
					"raw": "{\r\n            \"threatType\": \"MALWARE\",\r\n            \"platformType\": \"ANY_PLATFORM\",\r\n            \"threatEntryType\": \"URL\"\r\n        }",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "https://sba.yandex.net/v4/threatMatches:find",
					"protocol": "https",
					"host": [
						"sba",
						"yandex",
						"net"
					],
					"path": [
						"v4",
						"threatMatches:find"
					],
					"query": [
						{
							"key": null,
							"value": "40d9595f-997b-4b27-ad1e-a1ee63461dfd",
							"disabled": true
						}
					]
				}
			},
			"response": []
		},
		{
			"name": "проверкаURL2",
			"request": {
				"method": "POST",
				"header": [
					{
						"key": "Cookie",
						"value": "token_global={{token_global}}",
						"type": "text"
					}
				],
				"body": {
					"mode": "raw",
					"raw": " {\r\n            \"threatType\": \"MALWARE\",\r\n            \"platformType\": \"ANY_PLATFORM\",\r\n            \"threatEntryType\": \"URL\"\r\n        }",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "https://sba.yandex.net/v4/threatMatches:find",
					"protocol": "https",
					"host": [
						"sba",
						"yandex",
						"net"
					],
					"path": [
						"v4",
						"threatMatches:find"
					],
					"query": [
						{
							"key": null,
							"value": "40d9595f-997b-4b27-ad1e-a1ee63461dfd",
							"disabled": true
						}
					]
				}
			},
			"response": []
		}
	],
	"event": [
		{
			"listen": "prerequest",
			"script": {
				"type": "text/javascript",
				"exec": [
					""
				]
			}
		},
		{
			"listen": "test",
			"script": {
				"type": "text/javascript",
				"exec": [
					""
				]
			}
		}
	],
	"variable": [
		{
			"key": "token_global",
			"value": "40d9595f-997b-4b27-ad1e-a1ee63461dfd",
			"type": "string"
		},
		{
			"key": "baseURL",
			"value": "https://sba.yandex.net/v4/threatLists",
			"type": "string"
		}
	]
}lection.json…]()



# задача 2

Дано: корзина магазина “читай-город”

Необходимо: 

Составить коллекцию Postman с 4 основными действиями:

Добавление одной единицы товара в корзину.

Изменение количества одного товара в корзине.

Просмотр товаров в корзине.

Удаление товара из корзины.


Решение:

Заходим на сайт https://www.chitai-gorod.ru/cart  и открываем консоль разработчика,
ищем нужный URl и вставляем его в Postman, выполняем запрос на добавление одной единицы товара в корзину, в коллекции создаем запросы изменение количества одного товара в корзине, просмотр товаров в корзине, удаление товара из корзины.

Результат:

[Uploading читай-город.pos{
	"info": {
		"_postman_id": "90b5bc70-5bce-45b1-bc5b-13b5d66d7fad",
		"name": "читай-город",
		"schema": "https://schema.getpostman.com/json/collection/v2.1.0/collection.json",
		"_exporter_id": "25548534",
		"_collection_link": "https://cloudy-station-174388.postman.co/workspace/1~19e4b7a3-6081-43da-be17-1ec69151f246/collection/25548534-90b5bc70-5bce-45b1-bc5b-13b5d66d7fad?action=share&source=collection_link&creator=25548534"
	},
	"item": [
		{
			"name": "добавление товара в корзину",
			"request": {
				"method": "POST",
				"header": [
					{
						"key": "authority",
						"value": "web-gate.chitai-gorod.ru"
					},
					{
						"key": "accept",
						"value": "application/json, text/plain, */*"
					},
					{
						"key": "accept-language",
						"value": "ru-RU,ru;q=0.9,en-US;q=0.8,en;q=0.7"
					},
					{
						"key": "authorization",
						"value": "Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwczovL3VzZXItcmlnaHQiLCJzdWIiOjE5OTE1MjI3LCJpYXQiOjE2OTY1ODk5NjYsImV4cCI6MTY5NjU5MzU2NiwidHlwZSI6MjB9.0qjxExG-6oFHE0Yr433IPAzWiF8oIOJoFE0Sb3u8_zI"
					},
					{
						"key": "cache-control",
						"value": "no-store, no-cache, must-revalidate, proxy-revalidate, max-age=0"
					},
					{
						"key": "content-type",
						"value": "application/json"
					},
					{
						"key": "cookie",
						"value": "__ddg1_=PEFFt2YA7OHhOE4drADl; chg_visitor_id=43707320-9c93-4526-bd27-9e46e72656c4; _ym_uid=1696177337507341060; _ym_d=1696177337; _ga=GA1.1.636264354.1696177337; tmr_lvid=67e696c956cc6678fbe7df7c0678b6ae; tmr_lvidTS=1696177337598; popmechanic_sbjs_migrations=popmechanic_1418474375998%3D1%7C%7C%7C1471519752600%3D1%7C%7C%7C1471519752605%3D1; __ddg2_=5RhkF3fMt21OpKwJ; refresh-token=iGLjZnEP602TTSGwztx1ysNYLFgMOQy1nQjZCQg1rpJmfvccwOHLFaQwufv7BgW70S881NQsAzDWkMKy; _gpVisits={\"isFirstVisitDomain\":true,\"idContainer\":\"100025BD\"}; _ym_isad=1; access-token=Bearer%20eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwczovL3VzZXItcmlnaHQiLCJzdWIiOjE5OTE1MjI3LCJpYXQiOjE2OTY1ODk5NjYsImV4cCI6MTY5NjU5MzU2NiwidHlwZSI6MjB9.0qjxExG-6oFHE0Yr433IPAzWiF8oIOJoFE0Sb3u8_zI; _gp100025BD={\"hits\":31,\"vc\":1,\"ac\":1,\"a6\":1}; digi_uc=W1sidiIsIjMwMDQ1ODAiLDE2OTY0NDI5NzE2MTBdLFsidiIsIjI5ODA1MjkiLDE2OTY0NDI5MTUxMjldLFsidiIsIlxuICAgICAgICAzMDAxNTM2XG4gICAgICAiLDE2OTYzNDE5Nzc1NzhdLFsidiIsIlxuICAgICAgICA4MDAyOTYwXG4gICAgICAiLDE2OTYzNDEwMjY5OTZdLFsidiIsIjI3NjMyNTYiLDE2OTYzMzQzOTk0ODBdLFsidiIsIlxuICAgICAgICAyOTkzMzgzXG4gICAgICAiLDE2OTYyNTY4MjExNTNdLFsidiIsIjI5OTMzODMiLDE2OTYyNTI0NTUyMTddLFsidiIsIlxuICAgICAgICAyOTgwNTI5XG4gICAgICAiLDE2OTY1OTAwNTc3MjBdXQ==; _ga_W0V3RXZCPY=GS1.1.1696585622.9.1.1696590059.0.0.0; _ga_LN4Z31QGF4=GS1.1.1696585622.9.1.1696590059.47.0.0; mindboxDeviceUUID=8e93a719-70f1-4a7e-a785-3455fd1b18d7; directCrm-session=%7B%22deviceGuid%22%3A%228e93a719-70f1-4a7e-a785-3455fd1b18d7%22%7D"
					},
					{
						"key": "origin",
						"value": "https://www.chitai-gorod.ru"
					},
					{
						"key": "referer",
						"value": "https://www.chitai-gorod.ru/"
					},
					{
						"key": "sec-ch-ua",
						"value": "\"Google Chrome\";v=\"117\", \"Not;A=Brand\";v=\"8\", \"Chromium\";v=\"117\""
					},
					{
						"key": "sec-ch-ua-mobile",
						"value": "?0"
					},
					{
						"key": "sec-ch-ua-platform",
						"value": "\"Windows\""
					},
					{
						"key": "sec-fetch-dest",
						"value": "empty"
					},
					{
						"key": "sec-fetch-mode",
						"value": "cors"
					},
					{
						"key": "sec-fetch-site",
						"value": "same-site"
					},
					{
						"key": "user-agent",
						"value": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/117.0.0.0 Safari/537.36"
					}
				],
				"body": {
					"mode": "raw",
					"raw": "{\r\n    \"id\": 2980529,\r\n    \"adData\": {\r\n        \"item_list_name\": \"product-page\",\r\n        \"product_shelf\": \"\"\r\n    }\r\n}"
				},
				"url": {
					"raw": "{{baseURL}}/product",
					"host": [
						"{{baseURL}}"
					],
					"path": [
						"product"
					]
				}
			},
			"response": []
		},
		{
			"name": "изменение кол-во товаров в корзине",
			"request": {
				"method": "PUT",
				"header": [
					{
						"key": "authority",
						"value": "web-gate.chitai-gorod.ru"
					},
					{
						"key": "accept",
						"value": "application/json, text/plain, */*"
					},
					{
						"key": "accept-language",
						"value": "ru-RU,ru;q=0.9,en-US;q=0.8,en;q=0.7"
					},
					{
						"key": "authorization",
						"value": "Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwczovL3VzZXItcmlnaHQiLCJzdWIiOjE5OTE1MjI3LCJpYXQiOjE2OTY1ODk5NjYsImV4cCI6MTY5NjU5MzU2NiwidHlwZSI6MjB9.0qjxExG-6oFHE0Yr433IPAzWiF8oIOJoFE0Sb3u8_zI"
					},
					{
						"key": "cache-control",
						"value": "no-store, no-cache, must-revalidate, proxy-revalidate, max-age=0"
					},
					{
						"key": "content-type",
						"value": "application/json"
					},
					{
						"key": "cookie",
						"value": "__ddg1_=PEFFt2YA7OHhOE4drADl; chg_visitor_id=43707320-9c93-4526-bd27-9e46e72656c4; _ym_uid=1696177337507341060; _ym_d=1696177337; _ga=GA1.1.636264354.1696177337; tmr_lvid=67e696c956cc6678fbe7df7c0678b6ae; tmr_lvidTS=1696177337598; popmechanic_sbjs_migrations=popmechanic_1418474375998%3D1%7C%7C%7C1471519752600%3D1%7C%7C%7C1471519752605%3D1; __ddg2_=5RhkF3fMt21OpKwJ; refresh-token=iGLjZnEP602TTSGwztx1ysNYLFgMOQy1nQjZCQg1rpJmfvccwOHLFaQwufv7BgW70S881NQsAzDWkMKy; _gpVisits={\"isFirstVisitDomain\":true,\"idContainer\":\"100025BD\"}; _ym_isad=1; access-token=Bearer%20eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwczovL3VzZXItcmlnaHQiLCJzdWIiOjE5OTE1MjI3LCJpYXQiOjE2OTY1ODk5NjYsImV4cCI6MTY5NjU5MzU2NiwidHlwZSI6MjB9.0qjxExG-6oFHE0Yr433IPAzWiF8oIOJoFE0Sb3u8_zI; digi_uc=W1sidiIsIlxuICAgICAgICAyOTgwNTI5XG4gICAgICAiLDE2OTY1OTAxOTgzNTVdLFsidiIsIjMwMDQ1ODAiLDE2OTY0NDI5NzE2MTBdLFsidiIsIjI5ODA1MjkiLDE2OTY1OTA1MTc2MjZdLFsidiIsIlxuICAgICAgICAzMDAxNTM2XG4gICAgICAiLDE2OTYzNDE5Nzc1NzhdLFsidiIsIlxuICAgICAgICA4MDAyOTYwXG4gICAgICAiLDE2OTYzNDEwMjY5OTZdLFsidiIsIjI3NjMyNTYiLDE2OTYzMzQzOTk0ODBdLFsidiIsIlxuICAgICAgICAyOTkzMzgzXG4gICAgICAiLDE2OTYyNTY4MjExNTNdLFsidiIsIjI5OTMzODMiLDE2OTYyNTI0NTUyMTddXQ==; _ga_W0V3RXZCPY=GS1.1.1696585622.9.1.1696590963.0.0.0; _gp100025BD={\"hits\":38,\"vc\":1,\"ac\":1,\"a6\":1}; mindboxDeviceUUID=8e93a719-70f1-4a7e-a785-3455fd1b18d7; directCrm-session=%7B%22deviceGuid%22%3A%228e93a719-70f1-4a7e-a785-3455fd1b18d7%22%7D; _ga_LN4Z31QGF4=GS1.1.1696585622.9.1.1696590973.50.0.0"
					},
					{
						"key": "origin",
						"value": "https://www.chitai-gorod.ru"
					},
					{
						"key": "referer",
						"value": "https://www.chitai-gorod.ru/"
					},
					{
						"key": "sec-ch-ua",
						"value": "\"Google Chrome\";v=\"117\", \"Not;A=Brand\";v=\"8\", \"Chromium\";v=\"117\""
					},
					{
						"key": "sec-ch-ua-mobile",
						"value": "?0"
					},
					{
						"key": "sec-ch-ua-platform",
						"value": "\"Windows\""
					},
					{
						"key": "sec-fetch-dest",
						"value": "empty"
					},
					{
						"key": "sec-fetch-mode",
						"value": "cors"
					},
					{
						"key": "sec-fetch-site",
						"value": "same-site"
					},
					{
						"key": "user-agent",
						"value": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/117.0.0.0 Safari/537.36"
					}
				],
				"body": {
					"mode": "raw",
					"raw": "[\r\n    {\r\n        \"id\": 84918216,\r\n        \"quantity\": 7\r\n    }\r\n]"
				},
				"url": {
					"raw": "{{baseURL}}",
					"host": [
						"{{baseURL}}"
					]
				}
			},
			"response": []
		},
		{
			"name": "просмотр товаров в корзине",
			"request": {
				"method": "GET",
				"header": [
					{
						"key": "authority",
						"value": "web-gate.chitai-gorod.ru"
					},
					{
						"key": "accept",
						"value": "application/json, text/plain, */*"
					},
					{
						"key": "accept-language",
						"value": "ru-RU,ru;q=0.9,en-US;q=0.8,en;q=0.7"
					},
					{
						"key": "authorization",
						"value": "Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwczovL3VzZXItcmlnaHQiLCJzdWIiOjE5OTE1MjI3LCJpYXQiOjE2OTY1ODk5NjYsImV4cCI6MTY5NjU5MzU2NiwidHlwZSI6MjB9.0qjxExG-6oFHE0Yr433IPAzWiF8oIOJoFE0Sb3u8_zI"
					},
					{
						"key": "cache-control",
						"value": "no-store, no-cache, must-revalidate, proxy-revalidate, max-age=0"
					},
					{
						"key": "cookie",
						"value": "__ddg1_=PEFFt2YA7OHhOE4drADl; chg_visitor_id=43707320-9c93-4526-bd27-9e46e72656c4; _ym_uid=1696177337507341060; _ym_d=1696177337; _ga=GA1.1.636264354.1696177337; tmr_lvid=67e696c956cc6678fbe7df7c0678b6ae; tmr_lvidTS=1696177337598; popmechanic_sbjs_migrations=popmechanic_1418474375998%3D1%7C%7C%7C1471519752600%3D1%7C%7C%7C1471519752605%3D1; __ddg2_=5RhkF3fMt21OpKwJ; refresh-token=iGLjZnEP602TTSGwztx1ysNYLFgMOQy1nQjZCQg1rpJmfvccwOHLFaQwufv7BgW70S881NQsAzDWkMKy; _gpVisits={\"isFirstVisitDomain\":true,\"idContainer\":\"100025BD\"}; _ym_isad=1; access-token=Bearer%20eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwczovL3VzZXItcmlnaHQiLCJzdWIiOjE5OTE1MjI3LCJpYXQiOjE2OTY1ODk5NjYsImV4cCI6MTY5NjU5MzU2NiwidHlwZSI6MjB9.0qjxExG-6oFHE0Yr433IPAzWiF8oIOJoFE0Sb3u8_zI; digi_uc=W1sidiIsIlxuICAgICAgICAyOTgwNTI5XG4gICAgICAiLDE2OTY1OTAxOTgzNTVdLFsidiIsIjMwMDQ1ODAiLDE2OTY0NDI5NzE2MTBdLFsidiIsIjI5ODA1MjkiLDE2OTY1OTA1MTc2MjZdLFsidiIsIlxuICAgICAgICAzMDAxNTM2XG4gICAgICAiLDE2OTYzNDE5Nzc1NzhdLFsidiIsIlxuICAgICAgICA4MDAyOTYwXG4gICAgICAiLDE2OTYzNDEwMjY5OTZdLFsidiIsIjI3NjMyNTYiLDE2OTYzMzQzOTk0ODBdLFsidiIsIlxuICAgICAgICAyOTkzMzgzXG4gICAgICAiLDE2OTYyNTY4MjExNTNdLFsidiIsIjI5OTMzODMiLDE2OTYyNTI0NTUyMTddXQ==; _gp100025BD={\"hits\":43,\"vc\":1,\"ac\":1,\"a6\":1}; mindboxDeviceUUID=8e93a719-70f1-4a7e-a785-3455fd1b18d7; directCrm-session=%7B%22deviceGuid%22%3A%228e93a719-70f1-4a7e-a785-3455fd1b18d7%22%7D; _ga_LN4Z31QGF4=GS1.1.1696585622.9.1.1696591340.59.0.0; _ga_W0V3RXZCPY=GS1.1.1696585622.9.1.1696591341.0.0.0"
					},
					{
						"key": "origin",
						"value": "https://www.chitai-gorod.ru"
					},
					{
						"key": "referer",
						"value": "https://www.chitai-gorod.ru/"
					},
					{
						"key": "sec-ch-ua",
						"value": "\"Google Chrome\";v=\"117\", \"Not;A=Brand\";v=\"8\", \"Chromium\";v=\"117\""
					},
					{
						"key": "sec-ch-ua-mobile",
						"value": "?0"
					},
					{
						"key": "sec-ch-ua-platform",
						"value": "\"Windows\""
					},
					{
						"key": "sec-fetch-dest",
						"value": "empty"
					},
					{
						"key": "sec-fetch-mode",
						"value": "cors"
					},
					{
						"key": "sec-fetch-site",
						"value": "same-site"
					},
					{
						"key": "user-agent",
						"value": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/117.0.0.0 Safari/537.36"
					}
				],
				"url": {
					"raw": "{{baseURL}}",
					"host": [
						"{{baseURL}}"
					]
				}
			},
			"response": []
		},
		{
			"name": "удаление товара",
			"request": {
				"method": "DELETE",
				"header": [
					{
						"key": "authority",
						"value": "web-gate.chitai-gorod.ru"
					},
					{
						"key": "accept",
						"value": "application/json, text/plain, */*"
					},
					{
						"key": "accept-language",
						"value": "ru-RU,ru;q=0.9,en-US;q=0.8,en;q=0.7"
					},
					{
						"key": "authorization",
						"value": "Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwczovL3VzZXItcmlnaHQiLCJzdWIiOjE5OTE1MjI3LCJpYXQiOjE2OTY1ODk5NjYsImV4cCI6MTY5NjU5MzU2NiwidHlwZSI6MjB9.0qjxExG-6oFHE0Yr433IPAzWiF8oIOJoFE0Sb3u8_zI"
					},
					{
						"key": "cache-control",
						"value": "no-store, no-cache, must-revalidate, proxy-revalidate, max-age=0"
					},
					{
						"key": "cookie",
						"value": "__ddg1_=PEFFt2YA7OHhOE4drADl; chg_visitor_id=43707320-9c93-4526-bd27-9e46e72656c4; _ym_uid=1696177337507341060; _ym_d=1696177337; _ga=GA1.1.636264354.1696177337; tmr_lvid=67e696c956cc6678fbe7df7c0678b6ae; tmr_lvidTS=1696177337598; popmechanic_sbjs_migrations=popmechanic_1418474375998%3D1%7C%7C%7C1471519752600%3D1%7C%7C%7C1471519752605%3D1; __ddg2_=5RhkF3fMt21OpKwJ; refresh-token=iGLjZnEP602TTSGwztx1ysNYLFgMOQy1nQjZCQg1rpJmfvccwOHLFaQwufv7BgW70S881NQsAzDWkMKy; _gpVisits={\"isFirstVisitDomain\":true,\"idContainer\":\"100025BD\"}; _ym_isad=1; access-token=Bearer%20eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwczovL3VzZXItcmlnaHQiLCJzdWIiOjE5OTE1MjI3LCJpYXQiOjE2OTY1ODk5NjYsImV4cCI6MTY5NjU5MzU2NiwidHlwZSI6MjB9.0qjxExG-6oFHE0Yr433IPAzWiF8oIOJoFE0Sb3u8_zI; digi_uc=W1sidiIsIlxuICAgICAgICAyOTgwNTI5XG4gICAgICAiLDE2OTY1OTAxOTgzNTVdLFsidiIsIjMwMDQ1ODAiLDE2OTY0NDI5NzE2MTBdLFsidiIsIjI5ODA1MjkiLDE2OTY1OTA1MTc2MjZdLFsidiIsIlxuICAgICAgICAzMDAxNTM2XG4gICAgICAiLDE2OTYzNDE5Nzc1NzhdLFsidiIsIlxuICAgICAgICA4MDAyOTYwXG4gICAgICAiLDE2OTYzNDEwMjY5OTZdLFsidiIsIjI3NjMyNTYiLDE2OTYzMzQzOTk0ODBdLFsidiIsIlxuICAgICAgICAyOTkzMzgzXG4gICAgICAiLDE2OTYyNTY4MjExNTNdLFsidiIsIjI5OTMzODMiLDE2OTYyNTI0NTUyMTddXQ==; _ga_W0V3RXZCPY=GS1.1.1696585622.9.1.1696592108.0.0.0; _gp100025BD={\"hits\":54,\"vc\":1,\"ac\":1,\"a6\":1}; _ga_LN4Z31QGF4=GS1.1.1696585622.9.1.1696592113.54.0.0; mindboxDeviceUUID=8e93a719-70f1-4a7e-a785-3455fd1b18d7; directCrm-session=%7B%22deviceGuid%22%3A%228e93a719-70f1-4a7e-a785-3455fd1b18d7%22%7D"
					},
					{
						"key": "origin",
						"value": "https://www.chitai-gorod.ru"
					},
					{
						"key": "referer",
						"value": "https://www.chitai-gorod.ru/"
					},
					{
						"key": "sec-ch-ua",
						"value": "\"Google Chrome\";v=\"117\", \"Not;A=Brand\";v=\"8\", \"Chromium\";v=\"117\""
					},
					{
						"key": "sec-ch-ua-mobile",
						"value": "?0"
					},
					{
						"key": "sec-ch-ua-platform",
						"value": "\"Windows\""
					},
					{
						"key": "sec-fetch-dest",
						"value": "empty"
					},
					{
						"key": "sec-fetch-mode",
						"value": "cors"
					},
					{
						"key": "sec-fetch-site",
						"value": "same-site"
					},
					{
						"key": "user-agent",
						"value": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/117.0.0.0 Safari/537.36"
					}
				],
				"url": {
					"raw": "{{baseURL}}/product/84918216",
					"host": [
						"{{baseURL}}"
					],
					"path": [
						"product",
						"84918216"
					]
				}
			},
			"response": []
		}
	],
	"event": [
		{
			"listen": "prerequest",
			"script": {
				"type": "text/javascript",
				"exec": [
					""
				]
			}
		},
		{
			"listen": "test",
			"script": {
				"type": "text/javascript",
				"exec": [
					""
				]
			}
		}
	],
	"variable": [
		{
			"key": "baseURL",
			"value": "https://web-gate.chitai-gorod.ru/api/v1/cart",
			"type": "string"
		}
	]
}tman_collection.json…]()

