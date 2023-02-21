[strart process ](https://docs.camunda.org/manual/7.3/api-references/rest/?__hstc=252030934.37de7abe097d6b205e42c2d694cf22ad.1669306377086.1676631711179.1676906823972.5&__hssc=252030934.1.1676906823972&__hsfp=1456314816#process-definition-start-process-instance)
[camunda full stack archetecture ](https://www.youtube.com/watch?v=JlnRvH4Q7Fw)
[camunda variables in rest api](https://docs.camunda.org/manual/7.18/reference/rest/overview/variables/)


camunda forms references
formreference (process page ) = filenmae (project )= form ID (form page)

don't touch activity id


taskvariable



client generation

http://localhost:8081/engine-rest/process-definition/camunda-test2-process/start


formreference (process page ) = filenmae (project )= form ID (form page)

don't touch activity id


taskvariable



client generation

http://localhost:8081/engine-rest/process-definition/camunda-test2-process/start



formTask5 -> formVariable5
formTask4 -> formVariable4
formTask1 -> taskvariable
formTask3 -> nonn

Start process REST:

deploy process before starting it (attache form files when deploying )

method POST

url : http://localhost:8081/engine-rest/process-definition/camunda-test2-process:3:ab9f8fdc-b1d3-11ed-a23d-32d50dab7a5d/start

body 	:

{"variables":
{
"taskvariable" : {"value" : "", "type": "String"},
"formVariable4" : {"value" : "", "type": "String"},
"formVariable5" : {"value" : "", "type": "String"}
},
"businessKey" : ""
}

    

Get all Tasks :

http://localhost:8081/engine-rest/task

gets the current unclaimed tasks

Method GET


Get single task:

http://localhost:8081/engine-rest/task/{id}

gets the current unclaimed tasks

Method GET

get Task count :

Method GET
http://localhost:8081/engine-rest/task/count


Complete Task:

Method POST