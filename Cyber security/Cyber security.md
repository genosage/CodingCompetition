With all of the recent high profile cyber attacks on large companies, your company has decided to take proactive action to strengthen security measures. You have been tasked with devising a system that will limit access to sensitive documents, such as employee salaries, expense reports, and so on. A resource can be limited to only certain employees or to a group that contains employees. Groups can contain other groups and permissions should apply to all members; in particular, permission to a resource should be granted to any member of a group that has permission to the resource, regardless of whether the permission is direct or via nested group membership.

#### Input definition

The input will begin with two numbers: n (1 < n <= 1000) and m (1 < m < 100), where n is the number of groups in the system and m is the number of access checks to be made.

The first n lines after the first line will be the group definitions; they will be of the following format:

```
<name of group>:<name of member>;<name of second member>;<third & etc>
```

The following m lines will be the access checks and will be of the following format:

```
<name of user requesting access>;<group the member needs to be a part of>
```

Consider these group definitions:

```
Electronic Artists:Daft Punk;House DJs;Trance Kings
House DJs:Don Diablo;Tritonal;Hardwell
Trance Kings:Above & Beyond;Super8 & Tab
```

Daft Punk is a direct member of the group Electronic Artists and Hardwell is an indirect member. Any resource that permitted access to members of Electronic Artists would permit access to those two users (along with the group's other direct and indirect members). A resource that restricted access only to members of House DJs, however, would not include Daft Punk or Above & Beyond.

Consider these access checks:

```
Tritonal:Electronic Artists
Above & Beyond:House DJs
Super8 & Tab:Trance Kings
```

The first access check would be granted, although the membership is indirect. The second access check would be denied because Above & Beyond is not a direct or indirect member of House DJs. The third access check would be granted with a direct membership.

The system dictates that group memberships are not allowed to form a cycle.

#### Output definition

The output will contain m lines. The output is one of three possible values: Yes (direct), Yes (indirect) or No. The value to use depends on the result of the access check. If the access check was granted because the user was a direct member of the group, the output value should be Yes (direct). If the access check was granted because the user was an indirect member, the value should be Yes (indirect). If the access check was denied, the value should be No.

Continuing with the previous example, the output would be:

```
Yes (indirect)
No
Yes (direct)
```

#### Example input

```
6 6
Seahawks:Players;Coaching Staff;Owners;Paul Allen
Players:Russell Wilson;Marshawn Lynch (BEAST)
Coaching Staff:Pete Carroll
Owners:Paul Allen
Backup dancers:Left Shark;Right Shark
Halftime Show:Backup dancers;Katy Perry
Tom Brady;Seahawks
Left Shark;Halftime Show
Marshawn Lynch (BEAST);Seahawks
Pete Carroll;Coaching Staff
Katy Perry;Seahawks
Paul Allen;Seahawks
```

#### Example output

```
No
Yes (indirect)
Yes (indirect)
Yes (direct)
No
Yes (direct)
```