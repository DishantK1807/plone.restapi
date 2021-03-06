Types
=====

.. note::
    These docs are generated by code tests, therefore you will see some 'test' contenttypes appear here.

Available content types in a Plone site can be listed and queried by accessing the ``/@types`` endpoint on any context (requires an authenticated user). The 'addable' key specifies if the content type can be added to the current context.


..  http:example:: curl httpie python-requests
    :request: _json/types.req

.. literalinclude:: _json/types.resp
   :language: http



To get the schema of a content type, access the ``/@types`` endpoint  with the name of the content type, e.g. '/plone/@types/Document':

..  http:example:: curl httpie python-requests
    :request: _json/types_document.req

.. literalinclude:: _json/types_document.resp
   :language: http

The content type schema uses the `JSON Schema <http://json-schema.org/>`_ format.

See :ref:`types-schema` for a detailed documentation about the available field types.
