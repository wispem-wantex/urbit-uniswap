# Uniswap

This is Uniswap on Urbit.  Unlike previous versions of this app, there is no longer any configuration, proxy server, or any technical setup / dev-ops required. It just works.

A previous version of this app, made by @ajlamarc about a year ago, required an external proxy server, running alongside your Urbit ship, to circumvent CORS restrictions when querying the Uniswap graphql API.  It worked, but it was brittle.  My version builds on this work by moving the proxy server *inside* of Urbit (i.e., implementing a proxy agent as a Gall app) and bundling it with Uniswap.  Everything is handled invisibly by your ship, the way God intended it.

This represents a milestone in terms of front-end app deployments on Urbit, for several reasons.  To my knowledge, this is the first completely working DeFi frontend app deployed on Urbit.

But besides that, it showcases the strengths of Urbit as an app platform.  Publishing an app like this without Urbit would be difficult.  Why?  This app includes a static file bundle and two web services. Yet it requires no know-how to set up. You just paste in the link (in my 1st tweet) and click "Get app". And everything just happens.

This shows how Urbit can help achieve decentralization in practice, not just in theory.  In theory, Uniswap is open-source, and it's just a bunch of static HTML and JS files.  In practice, if you just deployed it naively, the connection would fail and it wouldn't work.

Urbit isn't just a file hosting server. It is that, but it's much *more* than that-- it's also an execution environment.  Even with something as simple as a pure-front-end JS app, you can use Urbit to improve the app, smooth over problems, and create a seamless user experience.

--

The proxy server leverages Urbit's Iris vane.  This and other aspects of the design was featured in an Urbit Developers Anonymous call, which can be watched on replay [here](https://twitter.com/urbitfoundation/status/1783195104083390641).
