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



  


