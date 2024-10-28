# employee_management_web_app
Solution to the project Build a CRUD Node.js and MongoDB employee management web-app available on [coursera][1]

## Frontend
The UI was done using the javascript/React framework [Vite][2]. The UI has 2 principal routes, /department and /employee. And make possible perform all the CRUD requests allowed to the API. The design is simple and have some responsivness.

The source code can be found at:
https://github.com/kvl-ballester/hospital_org_chart_frontend

## Backend
The API was done using the node framework express and uses [mongoose][3] ORM to connect to the mongo database.

The source code can be found at:
https://github.com/kvl-ballester/hospital_org_chart_frontend

## Data modeling
The project handles 2 colecctions, one for departments and another for employess. Departments consist of 2 fields, its name and an array of documents, which are an reduced version of the employee document. So there is a 1:n relation. The other colecction refers to employee and it has 3 fields, name, surname and department.

![Alt text](docs/models.png?raw=true "Title")

## How to compile locally
1. Clone the repo
2. Create api image
```
cd /api
docker build -t clinic-api .
```
3. Create frontend image
```
cd /frontend
docker build -t clinic-frontend .
```
4. Up containers
```
cd /compose
docker compose up
```
5. (optional) populate database
```
node /scripts/populateDb.js
```
Now, you can interact with the whole application through the browser at http://localhost:8080/




[1]: https://www.coursera.org/projects/showcase-build-a-crud-nodejs-and-mongodb-employee-management-web-app "coursera"
[2]: https://vite.dev/ "vite"
[3]: https://mongoosejs.com/ "mongoose"