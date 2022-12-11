
```
var console = console || {}; // just in case
console.watch = function(oObj, sProp) {
  var sPrivateProp = "$_"+sProp+"_$"; // to minimize the name clash risk
  oObj[sPrivateProp] = oObj[sProp];

  // overwrite with accessor
  Object.defineProperty(oObj, sProp, {
      get: function () {
          return oObj[sPrivateProp];
      },

      set: function (value) {
          //console.log("setting " + sProp + " to " + value);
          debugger; // sets breakpoint
          oObj[sPrivateProp] = value;
      }
  });
}
```

    Created at: 2021-07-02
    Updated at: 2021-07-02

