Frequently Asked Questions
##########################

The released YAML file doesn't build on my system. What can I do?
=================================================================

If you encounter an error when creating an environment from a YAML environment definition files built for a release (see :ref:`choose_release`),
you can try building an environment from the unconstrained ``environment.yaml`` file instead (:ref:`environment_definition`):

.. code-block:: shell

    conda env create --file https://raw.githubusercontent.com/spacetelescope/stenv/main/environment.yaml --name stenv

What about Astroconda?
======================

Astroconda, historically maintained by STScI as a Conda software channel, provides data analysis tools and pipelines via the Conda package management system.

.. warning::
    Astroconda is no longer supported as of **February 1st, 2023**.

``stenv`` supersedes Astroconda as a STScI software distribution; it supports most of the packages in Astroconda, works with all current versions of Python, and provides a common environment for both the Hubble Space Telescope (HST) and James Webb Space Telescope (JWST) pipelines.
Additionally, while Astroconda primarily uses Conda recipes to build and serve packages, which need to be updated separately from PyPI releases, ``stenv`` draws most of its packages directly from PyPI with ``pip`` (though it still requires use of a Conda environment for ``hstcal`` and ``fitsverify``, which are provided by ``conda-forge``).

