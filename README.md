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

[Uploading SafeBrow{
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
}sing.postman_collection.json…]()




# задача 2
