
# ------- commands for CRAB Job Submission ----------

cmsenv

voms-proxy-init -voms cms

voms-proxy-info -all | grep -Ei "role|subject"

source /cvmfs/cms.cern.ch/crab3/crab.csh

crab submit crab_config.py

crab status -d crablog_DIRECTORY

crab resubmit -d crablog_DIRECTORY

crab report -d crablog_DIRECTORY


# -------- To download -----------------------

git clone https://github.com/sandeepbhowmik1/CRABJobSubmission


# ------- Copy files for L1HPSTaus ----------

cp -r CRABJobSubmission/L1HPSTaus/crabsubmit $CMSSW_BASE/src/L1Trigger/Phase2L1Taus/test/
