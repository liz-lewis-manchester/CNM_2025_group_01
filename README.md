# CNM_2025_group_01
def_init_(self,U=0.1,dx=0.2,dt=10.0):
self._validate_parameters(U,dx,dt)

self.U=(U)
self.dx=(dx)
self.dt=(dt)

self.cfl=self.U*self.dt/self.dx\
self.is_stable=self.cfl<=0.1
