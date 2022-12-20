# SoapLecture18

SOAP web service accessing Contact record is added to this project
To call the service use this curl or wsdl from http://localhost:8080/ws/contacts.wsdl

curl --location --request POST 'localhost:8080/ws/' \
--header 'SOAPAction;' \
--data-raw '<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:gs="http://spring.io/guides/gs-producing-web-service">
   <soapenv:Header/>
   <soapenv:Body>
      <gs:getContactRequest>
         <gs:id>31</gs:id>
      </gs:getContactRequest>
   </soapenv:Body>
</soapenv:Envelope>'
