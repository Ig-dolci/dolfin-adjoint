# Change log

## dolfin-adjoint 2023.3.0 [2023-11-22]

- Downstream fixes for turning on annotations
- Use Github to build webpage
- Add [Code of conduct](./CODE_OF_CONDUCT.md)
- Auto-publishing PYPI images added

## dolfin-adjoint 2023.2.0 [2023-08-17]

- Remove firedrake_adjoint and pyadjoint from repo
- Simplify layout of code
- Use `src-layout``
- Use `pyproject.toml``

## dolfin-adjoint 2023.1.0 [2023-08-16]

- Compatible with [ufl-legacy](https://github.com/FEniCS/ufl-legacy)

## dolfin-adjoint 2023.0.0 [2023-08-16]

- Final release compatible with `ufl` pre [ufl-legacy](https://github.com/FEniCS/ufl-legacy)

## dolfin-adjoint 2019.1.0 [2019-05-27]

- Support for FEniCS 2019.1.0
- Added function `taylor_to_dict`, which automatically computes shape derivatives and hessians without user input
- Added support for shape optimization. Supports "naive" shape optimization, computing shape derivatives with the ufl function `CoordinateDerivative`, as well as more advanced optimization, where only the boundary mesh nodes are the design variables. Demo can be found in `examples/stokes-shape-ad`.
- Added support for `FunctionAssigner`
- Reintroduced tape visualisation to graphviz dot files
- Added support for KrylovSolver and PETScKrylovSolver

## dolfin-adjoint 2018.1.0 [2018-10-05]

- Support for FEniCS 2018.1.0

## dolfin-adjoint 2017.2.1 [2018-10-05]

- Merged `taylor_test` and `taylor_test_multiple`
- Use tensorflow for tape graph visualisation
- Add ROLSolver to pyadjoint optimization package
- Renamed ReducedFunctional.optimize to optimize_tape
- Now annotates function assignment of linear combinations
- create_overloaded_object is moved to pyadjoint, introducing the OverloadedType.\_ad_init_object method for the same purpose.
- Added UFLConstraint to dolfin-adjoint
- BlockVariable now has an attribute `marked_in_path`, which indicates if one needs to compute (adjoint/tlm/hessian) values for this block variable.
- Block.evaluate_adj and Block.evaluate_hessian now take a new bool argument `markings`, indicating if relevant block variables are marked.
- Added alternative Block methods for evaluating adjoint/tlm/hessian values, which hides some of the technical implementation details common for most evaluate\_\* Block methods.
- Add the class `Placeholder` to pyadjoint
- Add the method Control.tape_value for retrieving the value of an object on the tape

## dolfin-adjoint 2017.2.0 [2018-01-11]

- Initial release
