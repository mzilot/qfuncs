# Que Funcs

We want to run a function by diffrent arguments as parallel
Our resources have limitiation such as bandwith to download or process, therefore we set a limitaion to manage it

//qfuncs(data, maxTasks, func, callback)
--------------------------

var data = [18,4,16,24,3,8,45,3,12], sum = 0;


//maxTasks set to 4, its mean that we have 4 running functions at one time.

qfuncs(data, 4, function(item,nextp) {
  sum += item;
  nextp();
}, function(res) {
  console.log(sum)
});

# result
133
