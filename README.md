# my-social--network (forked after the ebook's git)

## nodemon, express, connect, socketio, mongodb, jade, backbone

node node_modules\nodemon\nodemon app.js
gets ("/")
render index.jade
index.jade <script> require.js
requirejs reads data-main attr
js/boot: loads all libs
js/boot: SocialNet.js initialize()
initialize() checkLogin w/ callback runApplication
checkLogin ajax account/authenticated (from app.js)
get("/account/authenticated") req.session.loggedIn true/false
socialnet callback change w/ location.hash

router.js (general Backbone router) searches the right #route as a string and creates a newView()
router.js as a define[] has an array of Backbone views and the same amount of functions for each view; LoginView() = views/login (a js in the front dir)
login.js -> asks for text version of templates/login.html places it as html() in #content block
ajax post /login
app.js sees that and sends Account.login()