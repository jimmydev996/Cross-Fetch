Universal WHATWG Fetch API for Node, Browsers, Workers and React Native. The scenario that cross-fetch really shines is when the same JavaScript codebase needs to run on different platforms.

- **Platform agnostic**: browsers, Node or React Native
- **Optional polyfill**: it's up to you if something is going to be added to the global object or not
- **Simple interface**: no instantiation, no configuration and no extra dependency
- **WHATWG compliant**: it works the same way wherever your code runs
- **TypeScript support**: better development experience with types.
- **Worker support**: works on different types of workers such as Service Workers and CloudFlare Workers

#### Yet another fetch library?

I did a lot of research in order to find a fetch library that could be simple, cross-platform and provide polyfill as an option. There's a plethora of libs out there but none could match those requirements.

#### Why polyfill might not be a good idea?

In a word? Risk. If the spec changes in the future, it might be problematic to debug. Read more about it on [sindresorhus's ponyfill](https://github.com/sindresorhus/ponyfill#how-are-ponyfills-better-than-polyfills) page. It's up to you if you're fine with it or not.

#### How does cross-fetch work?

Just like isomorphic-fetch, it is just a proxy. If you're in node, it delivers you the [node-fetch](https://github.com/bitinn/node-fetch/) library, if you're in a browser or React Native, it delivers you the github's [whatwg-fetch](https://github.com/github/fetch/). The same strategy applies whether you're using polyfill or ponyfill.


## Who's Using It?

|[![The New York Times](./docs/images/logo-nytimes.png)](https://www.nytimes.com/)|[![Apollo GraphQL](./docs/images/logo-apollo.png)](https://github.com/apollographql/apollo-client/)|[![Facebook](./docs/images/logo-facebook.png)](https://github.com/facebook/fbjs/)|[![Swagger](./docs/images/logo-swagger.png)](https://swagger.io/)|[![VulcanJS](./docs/images/logo-vulcanjs.png)](http://vulcanjs.org)|[![graphql-request](./docs/images/logo-graphql-request.png)](https://github.com/prisma/graphql-request)|
|:---:|:---:|:---:|:---:|:---:|:---:|
|The New York Times|Apollo GraphQL|Facebook|Swagger|VulcanJS|graphql-request|

