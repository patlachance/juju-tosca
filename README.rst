Juju Tosca
----------

An integration between Juju and OASIS Tosca YAML Simple Profile 1.0


Tosca Modeling
--------------

The TOSCA standard is modeled here as three distinct collections, The
meta model which per the standard is associated with a set of types,
and which is extensible by any given tosca file. The node templates
which are the actualization of the meta model as loaded from a tosca
yaml file. Finally the realized node resoures which are created by
an orchestrator and associated to their corresponding node templates.

The tosca standard has no formalized notion of realized topology
resources at this time.

This library chooses to map these distinct aggregates using
native python language constructs, meta models correspond to classes,
node templates to instances of those classes.


Execution
---------

The execution of the template takes place through three phases of binding


Input binding

Resource binding

The binding tier

tosca notes


Standards Questions
-------------------

 - what does a relation callout binding in a template look like.
 - relation shorthand form is not defined properly in the meta model
 - page 13 and 14 has requirements: database but elsewhere its database_endpoint

 Is this a typo.
 - wp_db_port: { get_ref_property: [ database_endpoint, database_endpoint, port ] }

 - page 9 points to an interface implementation artifact directly against the name
   of the interface instead of against the lifecycle operation.. there's some abmiguity
   here.

 - can more than one interface be associated to a type


Feedback
--------

 - os version should not be an integer, minimum it should be a float


library notes


- definition references interfaces by name in node, but by type in relation.
- a couple of typos
- capability matches node_type by bad name (should be types.nodes.Root)


questions

 - how does inheritance work across types, what inherits (properties, lifecycle)
 - spelling of endpoint vs database endpoint.
 - delete lifecycle operation [ is it normative, may have to combine with deletion]
 - mapping lifecycle to machine operations.. is start automatically re-invoked on boot?
 - is stopped launched before reboot?
 - order of relation lifecycle events

 - the xml policy notion

Binding to variables



