# abacus_insights
Provide an example of a SpringBoot REST service that conforms to the following specification.
Please include class UML diagram, sequence diagram, and unit tests where applicable.
Please include build instructions for building and running your application.

The application must support the following methods and endpoints:

* PUT    /resources/data
* GET    /resources/data/{data_id}
* DELETE /resources/data/{data_id}

{
  resourceType : Person,
  id : string,
  name : string,
  age : integer,
  locale : string
}

Test Cases for validation:

* Given the element of data is a Person, 
	when the system receives a PUT message, 
		then the data specified in the payload of the request is persisted to local storage 
		and an autogenerated id is added to the object and included in the response

* Given the person exists,
	when the system receives a GET message,
		then the system returns the json payload of the object in the response

* Given the person does not exist,
	when the system receives a GET message,
		then the system returns a HTTP 404 response

* Given the person exists,
	when the system receives a DELETE message,
		then the system returns a success message with the json payload of the object in the response

* Given the person does not exist,
	when the system receives a DELETE message,
		then the system returns a HTTP 404 response 