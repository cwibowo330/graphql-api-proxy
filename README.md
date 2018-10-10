# Using GraphQL as a proxy for existing API's example

- uses db.json for mock data 
http://localhost:3000/users
http://localhost:3000/users/1
http://localhost:3000/company
http://localhost:3000/company/1/users


- graphql server
http://localhost:4000/graphql
- npm run dev 
- npm run json:server


## EXAMPLES:
~~~~
query {
  users {
    firstName 
    age 
    company {
      id
    }
  }
}

query {
  user(id: "3") {
    firstName 
    age 
  }
}

query {
  company(id: "1") {
    id
    name
    description
    users {
      id
      firstName
    }
  }
}
~~~~
