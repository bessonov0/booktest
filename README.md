# Вступление

{% api-method method="get" host="https://api.cakes.com" path="/v1/cakes/:id" %}
{% api-method-summary %}
Get Cakes
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" %}
ID of the cake to get, for free of course.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=false %}
Authentication token to track down who is emptying our stocks.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="recipe" type="string" %}
The API will do its best to find a cake matching the provided recipe.
{% endapi-method-parameter %}

{% api-method-parameter name="gluten" type="boolean" required=true %}
Whether the cake should be gluten-free or not.
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```javascript
{
    "name": "Cake's name",
    "recipe": "Cake's recipe name",
    "cake": "Binary cake"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not find a cake matching this query.
{% endapi-method-response-example-description %}

```javascript
{
    "message": "Ain't no cake like that."
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

**Общие положения**

-  Битрикс ­­‑ одна из многочисленных систем класса CMS \(http://cmslist.ru/find\_cms/\), далеко не лучшая в своем классе \(конкуренты – навскидку – Drupal, Joomla\).  

- Популярна на территории СНГ, за пределами – отсутствует.

- Используется в основном для разработки интернет-магазинов, CRM, корпоративных порталов.

- На территории СНГ  Битрикс распространен за счет хорошего маркетинга \([пример](https://www.slideshare.net/bitrixcms1/ss-53642120)\) и агрессивного продвижения, особенно среди владельцев 1С, обещая:

- круглосуточную поддержку;

- легкую интеграцию с 1С;

- широкий выбор подрядчиков;

- достаточно большой «Магазин» \(маркет-плейс\), в котором можно купить готовые компоненты для своего сайта.



|  | **Java** | **Битрикс** |
| :--- | :--- | :--- |
| **Москва** | 3179 | 265 |
| **Санкт-Петербург** | 2711 | 89 |
| **Самара** | 171 | 15 |
| **Воронеж** | 137 | 1 |
| **Eссентуки** | 1 | 0 |



