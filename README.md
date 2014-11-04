demandware-angularjs-seed
=========================

# What this project is

This aims to provide a demo site showcasing the use of the [Open Commerce API](https://info.demandware.com/DOC1/topic/help/OCAPI/14.8/usage/OpenCommerceAPI.html?cp=0_9) (site requires login).

The Open Commerce API (short: OCAPI) is a [REST](http://en.wikipedia.org/wiki/Representational_state_transfer) programming interface for the Demandware platform. It is an alternative to the pipeline programming model, where you visually design an execution flow to be executed on the Demandware platform for each request. 

If you never heard of the [Demandware platform](https://www.demandware.com) you're still invited to look around here. But all documentation content, OCAPI access and more is currently restricted to developers who are already signed up, sorry.

This project is built using [AngularJS](https://angularjs.org/), the self-described "Superheroic JavaScript MVW Framework". There are [similar](https://github.com/opencodes/demandware-ocapi) [projects](https://github.com/nhduy1985/demandware-backbones-client) around, check them out.

Since OCAPI does not expose all features of a fully fledged Demandware powered store, yet, this demo site focuses on the parts we _can_ do right now (see [Features](#Features) below).

My personal pet peeve is performance tuning. So, please, if you find a way to do more with less send me a pull request.

# Quickstart

This assumes you already have the Node.js package manager (npm) installed. See [it's documentation](https://www.npmjs.org/doc/README.html) for how to do this.

```
git clone https://github.com/mattibickel/demandware-angularjs-seed.git
sudo npm install -g grunt-cli # skip this if you already have GruntJS
sudo npm install -g bower # skip this if you already have Bower
cd demandware-angularjs-seed
npm install
bower install
sed -e '/baseUrl/ s,base-url,http://api.example.com,' \
    -e '/apiVersion/ s,api-version,14.8,' \
    -e '/clientId/ s,client-id,1234,' \
    -e '/publicSiteUrl/ s,public-site-url,http://www.example.com,' \
    app/scripts/config.js.dist > app/scripts/config.js
grunt server
```

Of course you want to substitute your own sandbox URL for `baseUrl` and `publicSiteUrl`. You also need a `clientId`. This is a token that you generate in Account Manager, see [OCAPI client identification](https://info.demandware.com/DOC1/topic/help/OCAPI/14.8/usage/ClientApplicationIdentification.html?cp=0_9_0_1) for details.

 - Don't forget to add your development server to 'allowed_origins' in Business Manager.

# Features

- [x] Twitter Bootstrap 3.x (Inspired by http://www.bootstrapzero.com/bootstrap-template/mpurpose)
- [x] Responsive
- [x] Navigation menu
- [x] Show root categories 
- [x] Show category products
- [x] Show standard product detail page
- [ ] Show product page with complex data (variation, set, bundle)
- [ ] Shopping cart
- [ ] Checkout

# Screenshots:

Category page screenshot:
![alt text](https://raw.githubusercontent.com/nhduy1985/demandware-angularjs-seed/develop/screenshots/ss_category_1.png "Category Page")

Product page screenshot:
![alt text](https://raw.githubusercontent.com/nhduy1985/demandware-angularjs-seed/develop/screenshots/ss_product_1.png "Product Page")
