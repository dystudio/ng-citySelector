city selector based on AngularJS
====

ng-citySelector ��һ������AngularJS�ĳ���ѡ���������֧����ĸƴ����ѯ�ͺ��ֲ�ѯ��֧�ֻ�����ʷ������¼��֧�ֿ��ٶ�λ���

## Usage
�����ļ�����
```html
    <link rel="stylesheet" href="ng-city-selector.css">
    <script src="//cdn.bootcss.com/angular.js/1.5.0-beta.0/angular.min.js"></script>
    <script src="ng-citySelector.js"></script>
```
ģ������
```js
    var app = angular.module('myApp', ['ngCitySelector']);
```
HTMLʹ��
```html
    <ng-city-selector ng-cs-data="data" ng-cs-fn="select"></ng-city-selector>
```

### ����˵��:
|  ���� | ���� | ˵��
| ----- | ---- | ----
| ng-cs-data | Array | �������飬���ж���Ҫ�������������ֶΣ�{ name: '����',py: 'meiguo'}
| ng-cs-fn | Function | ������ѡ��ĳ�����к�ĵ���¼�������

### ʵ��

```js
var app = angular.module('myApp', ['ngCitySelector']);
app.controller('myCtrl', function($scope){
    $scope.data = [
        {
            name: '�й�',
            price: '9.9',
            en: 'cn',
            py: 'zhongguo'
        }, {
            name: '����',
            price: '9.9',
            en: 'en',
            py: 'meiguo'
        },
        ......
        {
            name: '�¼���',
            price: '9.9',
            en: 'en',
            py: 'xinjiapo'
        }
    ];

    $scope.select = function(v){
        console.log(v);
    };
});

```
Ч��ͼ��
ͼ1
![ͼ1](http://git.oa.com/jiangweixu/ng-citySelector/blob/master/imgs/1.png)
ͼ2
![ͼ2](http://git.oa.com/jiangweixu/ng-citySelector/blob/master/imgs/2.png)
ͼ3
![ͼ3](http://git.oa.com/jiangweixu/ng-citySelector/blob/master/imgs/3.png)

�ο�example
����[Demo](https://front-thinking.github.io/projects/ng-citySelector/)