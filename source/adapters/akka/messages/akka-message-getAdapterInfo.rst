.. _akka-message-getAdapterInfo:

obp.getAdapterInfo
===================

Gets information about the active general (non bank specific) Adapter that is responding to messages sent by OBP.

To query the most up to date message for your instance:


.. http:example:: curl wget httpie python-requests

   POST /obp/v3.1.0/users/current HTTP/1.1
   Host: YOUR-HOST
   Accept: application/json
   Authorization: DirectLogin token="abc123"


   HTTP/1.1 200 OK
   Content-Type: application/json

   {
     "user_id":"2ef35575-aae9-48fb-ad01-751755b3964f",
     "email":"Fred@example.com",
     "provider_id":"your-provider-id",
     "provider":"your-provider-name",
     "username":"fred",
     "entitlements":{"list":[]}
   }



.. list-table:: obp.getAdapterInfo
   :widths: 25 25 50
   :header-rows: 2

   * - Kafka/Akka 
     - Outbound
     - Inbound
   * - Topic
     - OutBoundGetAdapterInfo
     - InBoundGetAdapterInfo
   * - Message 
     - .. code-block:: json
         
          {
          "outboundAdapterCallContext":{
            "correlationId":"1flssoftxq0cr1nssr68u0mioj",
            "sessionId":"b4e0352a-9a0f-4bfa-b30b-9003aa467f50",
            "consumerId":"7uy8a7e4-6d02-40e3-a129-0b2bf89de8uh",
            "generalContext":[{
              "key":"5987953",
              "value":"FYIUYF6SUYFSD"
            }],
            "outboundAdapterAuthInfo":{
              "userId":"9ca9a7e4-6d02-40e3-a129-0b2bf89de9b1",
              "username":"felixsmith",
              "linkedCustomers":[{
                "customerId":"7uy8a7e4-6d02-40e3-a129-0b2bf89de8uh",
                "customerNumber":"5987953",
                "legalName":"Eveline Tripman"
              }],
              "userAuthContext":[{
                "key":"5987953",
                "value":"FYIUYF6SUYFSD"
              }],
              "authViews":[{
                "view":{
                  "id":"owner",
                  "name":"Owner",
                  "description":"This view is for the owner for the account."
                },
                "account":{
                  "id":"8ca8a7e4-6d02-40e3-a129-0b2bf89de9f0",
                  "accountRoutings":[{
                    "scheme":"IBAN",
                    "address":"DE91 1000 0000 0123 4567 89"
                  }],
                  "customerOwners":[{
                    "bankId":"GENODEM1GLS",
                    "customerId":"7uy8a7e4-6d02-40e3-a129-0b2bf89de8uh",
                    "customerNumber":"5987953",
                    "legalName":"Eveline Tripman",
                    "dateOfBirth":"2019-08-14T00:53:15Z"
                  }],
                  "userOwners":[{
                    "userId":"9ca9a7e4-6d02-40e3-a129-0b2bf89de9b1",
                    "emailAddress":"eveline@example.com",
                    "name":"felixsmith"
                  }]
                }
              }]
            }
          }
        }
     - .. code-block:: json
         
        {
          "inboundAdapterCallContext":{
            "correlationId":"1flssoftxq0cr1nssr68u0mioj",
            "sessionId":"b4e0352a-9a0f-4bfa-b30b-9003aa467f50",
            "generalContext":[{
              "key":"5987953",
              "value":"FYIUYF6SUYFSD"
            }]
          },
          "status":{
            "errorCode":"Status errorCode",
            "backendMessages":[{
              "source":"String",
              "status":"String",
              "errorCode":"String",
              "text":"String"
            }]
          },
          "data":{
            "errorCode":"",
            "backendMessages":[{
              "source":"String",
              "status":"String",
              "errorCode":"String",
              "text":"String"
            }],
            "name":"felixsmith",
            "version":"",
            "git_commit":"String",
            "date":"2017-09-19T02:31:05.000Z"
          }
        }

