# category-in-angularjs
angular.module('CategoryApp', [
  'CategoryApp.controllers',
  'CategoryApp.services',
  'ngRoute'

]).
config(['$routeProvider', function($routeProvider) {
  $routeProvider.
	when("/categories", {templateUrl: "partials/category.html", controller: "categoryController"}).
	when("/categories/:id", {templateUrl: "partials/category.html", controller: "categoryController"}).
	otherwise({redirectTo: '/categories'});
}]);
