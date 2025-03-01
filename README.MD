Setup: 

1. Install docker desktop 
   * Open command line `docker --version`
   * Optional: `docker pull wiremock/wiremock` 

2. Create a folder (repo) and it MUST HAVE this structure

**AnyProjectName**

* docker-compose.yml : default configuration; you can set any container name here.
* /__files
  * contains all response json files
* /mappings 
  * contains all endpoints and it should point to response json in __files folder

3. Open command line, go to the path of your wiremock project.
4. Bring up local server: `docker-compose up`
4. Call your endpoints:
   * you can use it in your automation
   * or on Postman
5. Bring down: `docker-compose down` 
or you can simply use docker desktop and click on stop button

For any changes in your mocks, you can click 'restart'