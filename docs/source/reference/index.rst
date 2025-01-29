API Reference for Optuna-Integration
====================================


The Optuna-Integration package contains classes used to integrate Optuna with external machine learning frameworks.

All of these classes can be imported in two ways. One is "`from optuna.integration import xxx`" like a module in Optuna,
and the other is "`from optuna_integration import xxx`" as an Optuna-Integration specific module.
The former is provided for backward compatibility.

For most of the ML frameworks supported by Optuna, the corresponding Optuna integration class serves only to implement a callback object and functions, compliant with the framework's specific callback API, to be called with each intermediate step in the model training. The functionality implemented in these callbacks across the different ML frameworks includes:

(1) Reporting intermediate model scores back to the Optuna trial using :meth:`optuna.trial.Trial.report`,
(2) According to the results of :meth:`optuna.trial.Trial.should_prune`, pruning the current model by raising :class:`optuna.TrialPruned`, and
(3) Reporting intermediate Optuna data such as the current trial number back to the framework, as done in :class:`~optuna_integration.MLflowCallback`.

For scikit-learn, an integrated :class:`~optuna_integration.OptunaSearchCV` estimator is available that combines scikit-learn BaseEstimator functionality with access to a class-level :class:`~optuna.study.Study` object.

AllenNLP
--------

.. autosummary::
   :toctree: generated/
   :nosignatures:

   optuna_integration.AllenNLPExecutor
   optuna_integration.allennlp.dump_best_config
   optuna_integration.AllenNLPPruningCallback

BoTorch
-------

.. autosummary::
   :toctree: generated/
   :nosignatures:

   optuna_integration.BoTorchSampler
   optuna_integration.botorch.ehvi_candidates_func
   optuna_integration.botorch.logei_candidates_func
   optuna_integration.botorch.qei_candidates_func
   optuna_integration.botorch.qnei_candidates_func
   optuna_integration.botorch.qkg_candidates_func
   optuna_integration.botorch.qehvi_candidates_func
   optuna_integration.botorch.qnehvi_candidates_func
   optuna_integration.botorch.qparego_candidates_func
   optuna_integration.botorch.qhvkg_candidates_func

CatBoost
--------

.. autosummary::
   :toctree: generated/
   :nosignatures:

   optuna_integration.CatBoostPruningCallback

Chainer
-------

.. autosummary::
   :toctree: generated/
   :nosignatures:

   optuna_integration.ChainerPruningExtension
   optuna_integration.ChainerMNStudy

Comet
-----

.. autosummary::
   :toctree: generated/
   :nosignatures:

   optuna_integration.CometCallback

Dask
----

.. autosummary::
   :toctree: generated/
   :nosignatures:

   optuna_integration.DaskStorage

fast.ai
-------

.. autosummary::
   :toctree: generated/
   :nosignatures:

   optuna_integration.FastAIV2PruningCallback
   optuna_integration.FastAIPruningCallback

Keras
-----

.. autosummary::
   :toctree: generated/
   :nosignatures:

   optuna_integration.KerasPruningCallback

LightGBM
--------

.. autosummary::
   :toctree: generated/
   :nosignatures:

   optuna_integration.LightGBMPruningCallback
   optuna_integration.lightgbm.train
   optuna_integration.lightgbm.LightGBMTuner
   optuna_integration.lightgbm.LightGBMTunerCV

MLflow
------

.. autosummary::
   :toctree: generated/
   :nosignatures:

   optuna_integration.MLflowCallback

MXNet
-----

.. autosummary::
   :toctree: generated/
   :nosignatures:

   optuna_integration.MXNetPruningCallback

pycma
-----
.. autosummary::
   :toctree: generated/
   :nosignatures:

   optuna_integration.PyCmaSampler

PyTorch
-------

.. autosummary::
   :toctree: generated/
   :nosignatures:

   optuna_integration.PyTorchIgnitePruningHandler
   optuna_integration.PyTorchLightningPruningCallback
   optuna_integration.TorchDistributedTrial

SHAP
----

.. autosummary::
   :toctree: generated/
   :nosignatures:

   optuna_integration.ShapleyImportanceEvaluator

sklearn
-------

.. autosummary::
   :toctree: generated/
   :nosignatures:

   optuna_integration.OptunaSearchCV

skorch
------

.. autosummary::
   :toctree: generated/
   :nosignatures:

   optuna_integration.SkorchPruningCallback

TensorBoard
-----------

.. autosummary::
   :toctree: generated/
   :nosignatures:

   optuna_integration.TensorBoardCallback

TensorFlow
----------

.. autosummary::
   :toctree: generated/
   :nosignatures:

   optuna_integration.TFKerasPruningCallback

Weights & Biases
----------------

.. autosummary::
   :toctree: generated/
   :nosignatures:

   optuna_integration.WeightsAndBiasesCallback

XGBoost
-------

.. autosummary::
   :toctree: generated/
   :nosignatures:

   optuna_integration.XGBoostPruningCallback
