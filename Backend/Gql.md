<h2><p align="center"> Tutorial Backend GraphQL </h2>
<hr/>

<div><h2>LifeCycle GraphQL & Mongoose <h2/></div>
<p>LifeCycle Method GQL, typeDefs => type Data, type Query , type Mutation</p>

<br> Module Npm <br>
npm i apollo-server <br>
npm i bcrypt<br>
npm i dotenv<br>
npm i graphql<br>
npm i jsonwebtoken<br>
npm i md5<br>
npm i mongoose<br>

<br>Devdependencies<br>
npm i concurrently --save<br>
npm i nodemon --save<br>
<br>
<br>

```javascript
const { ApolloServer, gql } = require("apollo-server");

const data = [
  { task: "Wash car", completed: false },
  { task: "Clean romm", completed: true }
];

/* LifeCycle Method GQL, typeDefs => type Data, type Query , type Mutation */

const typeDefs = gql`
  type Data {
    task: String
    completed: Boolean
  }

  type Query {
    getData: [Data]
  }

  type Mutation {
    addData(task: String, completed: Boolean): Data
  }
`;

// Function Object LifeCycle Method GQL
const resolvers = {
  Query: {
    getData: () => data
  },
  Mutation: {
    addData: (_, { task, completed }) => {
      const dataDummy = { task, completed };
      data.push(dataDummy);
      return dataDummy;
    }
  }
};

const server = new ApolloServer({
  typeDefs,
  resolvers
});

/* LifeCycle Method GQL, typeDefs => type Query , type Mutation */

server.listen().then(({ url }) => {
  console.log(`Server Has Been Connected on ${url}`);
});
```

<div>
    <p>
    How To Connected Database Moongose Mlab
    </p>
</div>

```javascript
const mongoose = require("mongoose");
// Create new file variable.env
MONGO_URL=mongodb://achmadsetiawannn:adfantage123@ds241408.mlab.com:41408/blog_db


require("dotenv").config({ path: "variables.env" });

mongoose
  .connect(process.env.MONGO_URL, { useNewUrlParser: true })
  .then(() => console.log("Database Has been connected"))
  .catch(err => console.log(err));
```

<hr/>
<div>
    <p>
    Lets Try and enjoy your life quotes. <br>
    #Dreamer, work hard and spend of time to learn code. make my dream come true.
    </p>
</div>
