```javascript
angular.module('moduleName', []).directive('directiveNameHere', function () {
    return {
        restrict: 'AECM',
        template: '<div></div>',
        replace: true,
        scope: {
                ngModel: '='
        },
        link: function (scope, element, attrs) {
            scope.$apply(function() {
                scope.ngModel = "Some data";
            });
        }
    };
});
```

```javascript
angular.module('moduleName', []).directive('directiveNameHere', function () {
    return {
        restrict: 'AECM',
        template: '<div></div>',
        replace: true,
        require: 'ngModel',
        link: function (scope, element, attrs, ngModel) {
            ngModel.$setViewValue("Some data");
            ngModel.$render();
            scope.$apply();
        }
    };
});
```

```javascript
angular.module('moduleName', []).directive('directiveNameHere', function () {
    return {
        restrict: 'AECM',
        template: '<div></div>',
        replace: true,
        require: 'ngModel',
        link: function (scope, element, attrs, ngModel) {
            scope.$apply(function(){
                ngModel.$setViewValue("Some data");
            });
        }
    };
});
```
