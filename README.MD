Setup: 

1. Install docker desktop 
   * Open command line `docker --version`
   * Get latest wiremock image: `docker pull wiremock/wiremock` 

2. Create a folder (repo) and it MUST HAVE this structure

**AnyProjectName**

* docker-compose.yml : default configuration; you can set any container name here.
* /__files
  * contains all response json files
* /mappings 
  * contains all endpoints and it should point to response json in __files folder

3. Open command line, go to the path of your wiremock project.
4. Bring up local mock server: `docker-compose up`
5. To check all available mappings: 
   `http://localhost:8080/__admin/mappings`
    * you can chose to use a different port #, just set it on your yaml file

7. Call your endpoints: 

. `http://localhost:8080/<yourUrlHere>`
   * you can use it in your automation
   * or on Postman


8. Bring down local mock server: `docker-compose down` 
or you can simply use docker desktop and click on stop button

For any changes in your mocks, you can click 'restart'

READ MORE
Request Matching samples/keywords: https://wiremock.org/docs/request-matching/