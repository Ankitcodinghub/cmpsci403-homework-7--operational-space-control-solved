# cmpsci403-homework-7--operational-space-control-solved
**TO GET THIS SOLUTION VISIT:** [CMPSCI403 Homework 7 -Operational Space Control Solved](https://www.ankitcodinghub.com/product/cmpsci-403-introduction-to-robotics-perception-mechanics-dynamics-and-control-solved-6/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;109284&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CMPSCI403 Homework 7 -Operational Space Control Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
In HW6, you made a dynamics simulation for the robot shown in Figure 1. Given a desired position of the foot rdC = [xd, yd]&gt;, your control law took the form:

. (1)

As we watched in the lecture, this method effectively controlled the position of the foot using a virtual spring-damper in task-space. However, the Jacobian was the only part of this control law that required information about the model! This homework will explore methods to improve the performance of the controller using more information about the model. Specifically, we will use information about its dynamics.

As we have seen in class, the dynamics of the leg are given by the configuration-space equations of motion:

M(q)q¨+ C(q,q˙) + G(q) = τ (2)

After a bit of algebraic manipulation, these equations can be rearranged into the operational-space equations of motion to describe the dynamics of the end-effector:

Λ(q)¨rC + µ(q,q˙) + ρ(q) = F (3)

where Λ(q) is the effective mass felt at the foot, µ(q,q˙) gives the coriolis and centripetal forces on the foot, and ρ(q) gives the gravity force felt on the foot. Formula for these quantities are given below:

Λ(q) = (JM−1JT)−1 (4)

µ(q,q˙) = ΛJM−1 C − ΛJ˙q˙ (5)

ρ(q) = ΛJM−1 G (6)

Figure 1: Double pendulum and parameter definitions.

1

In this assignment, you will explore the use of an extended version of Eq. 1 given by:

. (7)

Under mild assumptions, it can be show that the foot will converge to the desired trajectory with this control law.

1. Download the derive_eqns.m code. Using the simulate_pend.m code as a simulator, implement the control law in Eq. 7 in controller.m. The script derive_eqns.m creates a number of useful functions what will help in implementing the controller once you specify kinetic/potential energy and generalized forces.

With your operational space controller, run the circular trajectory tracking simulation. You should use parameters:

r (8)

ω = 2π rad/s (9)

(10)

(11)

(12)

(13)

Turn in a plot of of x, y, xd, and yd versus time.

2. Repeat step 2. using modified control laws:

• •

•

Turn in a plot of of x, y, xd, and yd versus time for each case. Also, include a short description of what is neglected in each controller, and how that relates with the observed performance. For comparison, you probably need to try different trajectory speed, link masses, or feedback gains.

3. Turn in your controller.m and derive_eqns.m code.

2
