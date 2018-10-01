---
description: тут тестируем коды
---

# Всякие коды

{% code-tabs %}
{% code-tabs-item title="test.kt" %}
```kotlin
fun testBulkInserts() {

        inSilence {

            val attach = Attach {
                it[name] = "test666"
                it["data"] = """
                    {
                    "type": "the doors",
                    "name": "A green door to \"knowhere\"",
                    "price": 3.50
                    }
                """.trim()
            }
            val attach2 = Attach {
                it[name] = "test777"
                it["data"] = "{}"
            }

            dataServiceExtd.bulkInsert(listOf(attach, attach2))
        }

        val check1 = dataService
                .find_(Attach.slice {
                    withBlobs()
                    filter { name eq "test666" }
                })
        println(check1.dataMapToString())
        assertEquals(check1["data.name"], "A green door to \"knowhere\"")


        val check2 = dataService
                .find_(Attach.slice {
                    
                    filter { name eq "test777" }
                })
        println(check2.dataMapToString())
        assertNotNull(check2["data"])
    }
```
{% endcode-tabs-item %}

{% code-tabs-item title="" %}
```

```
{% endcode-tabs-item %}
{% endcode-tabs %}

![&#x420;&#x43E;&#x434;&#x438;&#x43D;&#x430; &#x441;&#x43B;&#x44B;&#x448;&#x438;&#x442; - &#x412;&#x430;&#x441;&#x44F; &#x41B;&#x43E;&#x436;&#x43A;&#x438;&#x43D;](../../.gitbook/assets/22188-540x437.jpg)

тут тестируем [коды ](https://ru.wikipedia.org/wiki/%D0%9A%D0%BE%D0%B4)

{% file src="../../.gitbook/assets/analitiki.jpg" %}

{% page-ref page="./" %}

{% hint style="info" %}
Тут подскауываыва
{% endhint %}



* [ ] фывфы
* [x] фывфывыф
* [ ] фывфыв
* [ ] 
#### прарпарпар

```kotlin
package com.bftcom.ice.server.services

import com.bftcom.ice.common.maps.dataMapToString
import com.bftcom.ice.common.maps.inSilence
import com.bftcom.ice.server.Attach
import com.bftcom.ice.server.BaseSpringTests
import com.bftcom.ice.server.test.IfSpringProfileActive
import org.junit.Test
import kotlin.test.assertEquals


```

{% page-ref page="../1111/api.md" %}



