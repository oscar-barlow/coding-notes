[⬅︎ Back to Contents page](https://github.com/oscar-barlow/coding-notes#coding-notes)

---

# Object-oriented Design
###### Notes on Sandi Metz' book. Based on the 2013 edtition.

## Introduction
Software exists to do something; that's the whole point of it. Fortunately, the practices that produce the best software are also the practices that render making software enjoyable.

Change is unavoidable in software design, as in everything. It is the need to adapt to change that makes design matter. Applications that are easy to change are a joy to create and extend.

Object-oriented applications are made up of parts that interact to produce the behaviour of a whole (side note: would it be fair to describe this as a *system*?). Objects are the parts. They pass messages between them. Getting the right message to the right object requires that the sender knows some things about the receiver. This creates **dependencies** between the two objects.

Object-oriented design ('OOD') is about **managing dependencies**. Unmanaged dependencies wreak havoc because objects know too much about each other. Too much knowledge makes objects picky; it makes your system fragile. It makes things tough to test and to change.

You can get away with bad design in a small application the entirety of which you can hold in your head. But if that small application is successful, it will become a big application. Then the pain starts.

If you don't want your small application to be successful, why are you making it in the first place? Do OOD.

For any application, the cost of change will eclipse the original cost of delivering the application.

As a developer you must synthesize:

* Understanding of your application's requirements
* Costs and benefits of design alternatives

To produce an arrangement of code that is effective in the present and will continue to be so in the future.

As a general rule, it's not a good idea to anticipate *specific* future design requirements. **Rather seek to design in such a way that you can also design later. **Reduce the cost of change.

Design should be coupled to creation, not separated. It should include a timely and incremental feedback loop. No-one can envisage what an application will eventually do, as the design process informs it.

### Principles and Patterns
Design is not about rules. It is about making decisions. Thus your tools for software design are principles and patterns - things that help you make decisions.

#### Principles

Five of the most well-known principles of OOD are mnemonically known as **SOLID**, coined by Michael Feathers and popularised by Robert Martin:

1. **S**ingle Responsibility
2. **O**pen-Closed
3. **L**iskov Substitution
4. **I**nterface Segregation
5. **D**ependencey Inversion

Other principles include **DRY** (Don't Repeat Yourself) and **LoD** (the Law of Demeter).

These principles are good rules of thumb that originate from software developers' lived experiences writing code. Their value has also been validated by a number of academic studies.

#### Patterns
Patterns are simple and elegant solutions to very specific problems in OOD. The trick with patterns is to know when to choose and use them.

### Judging Design
There are plenty of Ruby gems that judge code against OOD principles and produce metrics about them. Bad metrics pretty much guarantee the application is badly designed. Good metrics do not guarantee the application is well-designed. This is because it is possible to write good code that over-anticipates the future, thus making it hard to change the applicaiton should the *actual* future turn out not to be the one that was anticipated. So OOD metrics should be taken with a pinch of salt.

The ideal measure of code quality would be *cost per feature over the time interval that matters.* This is nearly impossible to discern.

Time is a crucial ingredient. If it is vital that you produce a feature in a very short amount of time, you will likely make some compromises on design. You will probably have to deal with some of these compromises in the future, so making the compromise is kind of like taking time from the future. It's called **technical debt** and must usually be repaid with interest.

Your goal is to write software with the lowest cost-per feature. Therefore, your decision about how much design to do depends on two things: your skills and your timeframe.

If it takes ages to see a return on good design (either due to your skills or the timeframe you have in which to deliver), it may not be worth it. The better your skills, likely the sooner your break-even.

The rest of the book is about making the break-even ever more in your favour.


---
[⬅︎ Back to Contents page](https://github.com/oscar-barlow/coding-notes#coding-notes)
