An extremely basic example of a web form that publishes the form results to
a ROS message. Written for some research where I was collecting responses
from study participants, didn't want to make them type into a terminal, and
didn't want to have to take responses from them individually.

The package uses roslibjs and requires a running rosbridge server on the
machine pointed to in `collector.js`. On that machine, run

```
roslaunch rosbridge_server rosbridge_websocket.launch
```

Each time the form is submitted, a String mesage will be published to
the ROS topic `/user_response`. Note that the publishing can sometimes be
unreliable.