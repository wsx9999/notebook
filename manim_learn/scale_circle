class wsx(Scene):
    def construct(self):
        radius=ValueTracker(1)
        circle_1=Circle(radius=1).move_to(np.array([-1,0,0]))
        circle_2=Circle(radius=1).move_to(np.array([1,0,0]))
        self.add(circle_1,circle_2)        
        self.wait()
        circle_2.initial=circle_2.copy()
        def updater_circle(obj):
            obj.become(obj.initial)
            obj.scale(radius.get_value())
        circle_2.add_updater(updater_circle)
        self.add(circle_1,circle_2)
        self.play(radius.increment_value,2,run_time=2)
        self.wait()
