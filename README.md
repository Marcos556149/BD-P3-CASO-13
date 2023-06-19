# BD-P3-CASO-13
1*) A= π num σ provincia='San Luis' Sucursal
    B= π cod (Producto ⨝ A)
    Sucursal ⨝ (π num,cod Detalle ÷ B)
2*) A= π cod, provincia (Sucursal ⨝ Producto)
    B= A ⨝ Detalle
    C= π P,C ρ P ← provincia, C ← cod B
    D= C ⨯ π provincia, cod B
    π provincia σ provincia = P ∧ cod ≠ C D
3*) A= π cod σ nombre='Pizza napolitana' ∨ nombre='Pizza napolitana especial' Producto
    Sucursal ⨝ (π num,cod (Sucursal ⨝ Producto) ÷ A)
4*) A= π num σ provincia='San Juan' ∨ provincia='Mendoza' ∨ provincia='San Luis' Sucursal
    π nombre, stock (Producto ⨝ (π cod,num Producto ÷ A))
5*) A= π num σ nombre='Pizza muzzarella' Producto
    π provincia Sucursal - π provincia (Sucursal ⨝ A)
6*) A= π num σ nombre='Pizza con jamón' Producto
    π num Sucursal - A
7*) A= π num σ provincia='San Juan' Sucursal
    π nombre,num Producto ÷ A    
