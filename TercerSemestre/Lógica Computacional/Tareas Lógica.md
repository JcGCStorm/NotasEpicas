5. Aplica las sigs sustituciones y al finalizar elimina los paréntesis que sean redundantes. Muestra a detalle los pasos realizados.
	b) $(p \lor q) \implies ((¬r) \iff (p \iff s))$  $[r,p,q := p, p \land q, p \land q \land r]$
Sustituimos "r" por "p" 
$(p \lor q) \implies ((¬p) \iff (p \iff s))$ $[p,q := p \land q, p \land q \land r]$
Sustituimos "p" por  "$p \land q$"
$((p \land q) \lor q) \implies ((¬(p \land q)) \iff ((p \land q) \iff s))$ $[q := p \land q \land r]$
Sustituimos "q" por "$p \land q \land r$"
$((p \land (p \land q \land r)) \lor (p \land q \land r)) \implies ((¬(p \land (p \land q \land r))) \iff((p \land (p \land q \land r)) \iff s))$ 
Borramos los paréntesis innecesarios
$(p \land p \land q \land r \lor p \land q \land r)$ $\implies$ $(¬(p \land p \land q \land r) \iff ((p \land p \land q \land r) \iff s))$
 

d) $((q \land r)[q, p: = ¬p, s] \implies (r \land ¬(r \iff p)))$ $[r, p : = ¬r, s \land p]$
Sustituimos "q" por "¬p" solo de la primera sustitución.
$((¬p \land r)[p: = s] \implies (r \land ¬(r \iff p)))$ $[r, p : = ¬r, s \land p]$
Sustituimos "p" por "s"
$((¬s \land r)\implies (r \land ¬(r \iff p)))$ $[r, p : = ¬r, s \land p]$
Sustituimos "r" por ¬r
$((¬s \land ¬r)\implies (¬r \land ¬(¬r \iff p)))$ $[p : = s \land p]$
Sustituimos "p" por $s \land p$
$((¬s \land ¬r)\implies (¬r \land ¬(¬r \iff (s \land p))))$
Eliminamos paréntesis innecesarios
$(¬s \land ¬r)\implies (¬r \land ¬(¬r \iff (s \land p)))$


