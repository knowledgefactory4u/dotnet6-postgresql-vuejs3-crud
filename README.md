# .Net 6 + PostgreSQL + Vue.js 3 CRUD Application Example

# After completing this tutorial what we will build? 
We will build a full-stack web application that is a basic User Management Application with CRUD features: 

• Create User 

• List User 

• Update User 

• Delete User 

• View User

<img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhXevh3nQUi2t3WYNzgHxMTpz09YTBeLpAYceshPJ6iPag8BVB7ksc5kObDCstR7REpgn3FdZp3fV108sOES51clnDhlRDR9upcTd0FVDhMyNYFwrnsbsPEkykMPYDeTZT1H2HgIBc9ALBO3BUnCx2GZihCSN0vdQVFbBgpbkOjVjTeyrOtJPTL_HpFOw/w640-h276/listuser.png">


# Local Setup and Run the application

<h2>Create database and table</h2>

```CREATE DATABASE testdb;```

```
CREATE TABLE IF NOT EXISTS public.users
(
    id bigint NOT NULL DEFAULT nextval('users_id_seq'::regclass),
    email character varying(100) COLLATE pg_catalog."default",
    first_name character varying(100) COLLATE pg_catalog."default",
    last_name character varying COLLATE pg_catalog."default",
    CONSTRAINT primary_key_id PRIMARY KEY (id)
)
WITH (
    OIDS = FALSE
)
TABLESPACE pg_default;

ALTER TABLE IF EXISTS public.users
    OWNER to postgres;
```

<h2> Download or clone the source code from GitHub to the local machine</h2>

<h2> Backend</h2>

You can start the api by running ```dotnet run``` from the command line in the project root folder (where the WebApi.csproj file is located)

OR

You can also start the application in debug mode in Visual Studio by opening the project root folder in Visual Studio and pressing F5 or by selecting Debug -> Start Debugging from the top menu, running in debug mode.

<h2>Frontend</h2>

```npm install```

```npm run serve -- --port 8081```

<h2>From the browser call the endpoint http://localhost:8081/.</h2>


