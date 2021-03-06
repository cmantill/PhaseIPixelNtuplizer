include Makefile.arch
SrcSuf = cc

CXX  += -std=c++1z -fdiagnostics-color=always -Wall
LIBS += -lboost_system -lboost_filesystem

# Utility

CONSOLECOLORS_S = ./src/ConsoleColors.$(SrcSuf)
CONSOLECOLORS_O = ./obj/ConsoleColors.$(ObjSuf)
OBJS     += $(CONSOLECOLORS_O)

CONSOLEACTOR_S = ./src/ConsoleActor.$(SrcSuf)
CONSOLEACTOR_O = ./obj/ConsoleActor.$(ObjSuf)
OBJS     += $(CONSOLEACTOR_O)

COMMONACTORS_S = ./src/CommonActors.$(SrcSuf)
COMMONACTORS_O = ./obj/CommonActors.$(ObjSuf)
OBJS     += $(COMMONACTORS_O)

TIMER_S = ./src/Timer.$(SrcSuf)
TIMER_O = ./obj/Timer.$(ObjSuf)
OBJS     += $(TIMER_O)

TIMERCOL_S = ./src/TimerColored.$(SrcSuf)
TIMERCOL_O = ./obj/TimerColored.$(ObjSuf)
OBJS     += $(TIMERCOL_O)

TTREETOOLS_S = ./src/TTreeTools.$(SrcSuf)
TTREETOOLS_O = ./obj/TTreeTools.$(ObjSuf)
OBJS     += $(TTREETOOLS_O)

CANVASEXTRAS_S = ./src/CanvasExtras.$(SrcSuf)
CANVASEXTRAS_O = ./obj/CanvasExtras.$(ObjSuf)
OBJS     += $(CANVASEXTRAS_O)

TRAJMEAS_HISTOGRAM_FILLER_MODULE_S = ./src/TrajMeasHistogramFillerModule.$(SrcSuf)
TRAJMEAS_HISTOGRAM_FILLER_MODULE_O = ./obj/TrajMeasHistogramFillerModule.$(ObjSuf)
OBJS     += $(TRAJMEAS_HISTOGRAM_FILLER_MODULE_O)

FILTERCALIBRATION_MODULE_S = ./src/FilterCalibrationModule.$(SrcSuf)
FILTERCALIBRATION_MODULE_O = ./obj/FilterCalibrationModule.$(ObjSuf)
OBJS     += $(FILTERCALIBRATION_MODULE_O)

COSMIC_TRAJMEAS_HISTOS_MODULE_S = ./src/CosmicTrajMeasHistosModule.$(SrcSuf)
COSMIC_TRAJMEAS_HISTOS_MODULE_O = ./obj/CosmicTrajMeasHistosModule.$(ObjSuf)
OBJS     += $(COSMIC_TRAJMEAS_HISTOS_MODULE_O)

CLUSTEROCCUPANCY_MODULE_S = ./src/ClusterOccupancyModule.$(SrcSuf)
CLUSTEROCCUPANCY_MODULE_O = ./obj/ClusterOccupancyModule.$(ObjSuf)
OBJS     += $(CLUSTEROCCUPANCY_MODULE_O)

# PROGRAMS

EFFICIENCY_MAIN_S = ./src/efficiency_main.$(SrcSuf)
EFFICIENCY_MAIN_O = ./obj/efficiency_main.$(ObjSuf)
EFFICIENCY_MAIN_A = ./bin/efficiency_main$(ExeSuf)
OBJS     += $(EFFICIENCY_MAIN_O)
PROGRAMS += $(EFFICIENCY_MAIN_A)

EFFICIENCY_MULTIHITMEAS_S = ./src/efficiency_multiHitMeas.$(SrcSuf)
EFFICIENCY_MULTIHITMEAS_O = ./obj/efficiency_multiHitMeas.$(ObjSuf)
EFFICIENCY_MULTIHITMEAS_A = ./bin/efficiency_multiHitMeas$(ExeSuf)
OBJS     += $(EFFICIENCY_MULTIHITMEAS_O)
PROGRAMS += $(EFFICIENCY_MULTIHITMEAS_A)

EFFICIENCY_FILTERCALIBRATION_S = ./src/efficiency_filterCalibration.$(SrcSuf)
EFFICIENCY_FILTERCALIBRATION_O = ./obj/efficiency_filterCalibration.$(ObjSuf)
EFFICIENCY_FILTERCALIBRATION_A = ./bin/efficiency_filterCalibration$(ExeSuf)
OBJS     += $(EFFICIENCY_FILTERCALIBRATION_O)
PROGRAMS += $(EFFICIENCY_FILTERCALIBRATION_A)

COSMIC_MUON_PLOTTER_S = ./src/cosmicMuonPlotter.$(SrcSuf)
COSMIC_MUON_PLOTTER_O = ./obj/cosmicMuonPlotter.$(ObjSuf)
COSMIC_MUON_PLOTTER_A = ./bin/cosmicMuonPlotter$(ExeSuf)
OBJS     += $(COSMIC_MUON_PLOTTER_O)
PROGRAMS += $(COSMIC_MUON_PLOTTER_A)

MERGE_SIMHIT_PLOTS_S = ./src/mergeSimhitPlots.$(SrcSuf)
MERGE_SIMHIT_PLOTS_O = ./obj/mergeSimhitPlots.$(ObjSuf)
MERGE_SIMHIT_PLOTS_A = ./bin/mergeSimhitPlots$(ExeSuf)
OBJS     += $(MERGE_SIMHIT_PLOTS_O)
PROGRAMS += $(MERGE_SIMHIT_PLOTS_A)

DISK1_PROPAGATION_CHECK_S = ./src/disk1PropagationCheck.$(SrcSuf)
DISK1_PROPAGATION_CHECK_O = ./obj/disk1PropagationCheck.$(ObjSuf)
DISK1_PROPAGATION_CHECK_A = ./bin/disk1PropagationCheck$(ExeSuf)
OBJS     += $(DISK1_PROPAGATION_CHECK_O)
PROGRAMS += $(DISK1_PROPAGATION_CHECK_A) 

all: $(PROGRAMS)

# Executables

$(EFFICIENCY_MAIN_A): $(EFFICIENCY_MAIN_O) $(CONSOLECOLORS_O) $(CONSOLEACTOR_O) $(COMMONACTORS_O) $(TIMER_O) $(TIMERCOL_O) $(TTREETOOLS_O) $(CANVASEXTRAS_O)
	@printf "Compiling done, linking efficiency_main...\n"
	@$(LD) $(LDFLAGS) -Wall -Wshadow $^ $(LIBS) $(OutPutOpt)$@
	$(MT_EXE)
	@echo "Succesful make..."
	@echo "...$@ is ready to use."

$(EFFICIENCY_MULTIHITMEAS_A): $(EFFICIENCY_MULTIHITMEAS_O) $(CONSOLECOLORS_O) $(CONSOLEACTOR_O) $(COMMONACTORS_O) $(TIMER_O) $(TIMERCOL_O) $(TTREETOOLS_O) $(CANVASEXTRAS_O)
	@printf "Compiling done, linking efficiency_multiHitMeas...\n"
	@$(LD) $(LDFLAGS) -Wall -Wshadow $^ $(LIBS) $(OutPutOpt)$@
	$(MT_EXE)
	@echo "Succesful make..."
	@echo "...$@ is ready to use."

$(EFFICIENCY_FILTERCALIBRATION_A): $(EFFICIENCY_FILTERCALIBRATION_O) $(CONSOLECOLORS_O) $(CONSOLEACTOR_O) $(COMMONACTORS_O) $(TIMER_O) $(TIMERCOL_O) $(TTREETOOLS_O) $(CANVASEXTRAS_O) $(CLUSTEROCCUPANCY_MODULE_O) $(TRAJMEAS_HISTOGRAM_FILLER_MODULE_O) $(FILTERCALIBRATION_MODULE_O)
	@printf "Compiling done, linking efficiency_filterCalibration...\n"
	@$(LD) $(LDFLAGS) -Wall -Wshadow $^ $(LIBS) $(OutPutOpt)$@
	$(MT_EXE)
	@echo "Succesful make..."
	@echo "...$@ is ready to use."

$(COSMIC_MUON_PLOTTER_A): $(COSMIC_MUON_PLOTTER_O) $(CONSOLECOLORS_O) $(CONSOLEACTOR_O) $(COMMONACTORS_O) $(TIMER_O) $(TIMERCOL_O) $(TTREETOOLS_O) $(CANVASEXTRAS_O) $(CLUSTEROCCUPANCY_MODULE_O) $(TRAJMEAS_HISTOGRAM_FILLER_MODULE_O) $(COSMIC_TRAJMEAS_HISTOS_MODULE_O)
	@printf "Compiling done, linking cosmicMuonPlotter...\n"
	@$(LD) $(LDFLAGS) -Wall -Wshadow $^ $(LIBS) $(OutPutOpt)$@
	$(MT_EXE)
	@echo "Succesful make..."
	@echo "...$@ is ready to use."

$(MERGE_SIMHIT_PLOTS_A): $(MERGE_SIMHIT_PLOTS_O) $(CONSOLECOLORS_O) $(CONSOLEACTOR_O) $(COMMONACTORS_O) $(TIMER_O) $(TIMERCOL_O) $(TTREETOOLS_O) $(CANVASEXTRAS_O) $(CLUSTEROCCUPANCY_MODULE_O) $(TRAJMEAS_HISTOGRAM_FILLER_MODULE_O) $(FILTERCALIBRATION_MODULE_O)
	@printf "Compiling done, linking mergeSimhitPlots...\n"
	@$(LD) $(LDFLAGS) -Wall -Wshadow $^ $(LIBS) $(OutPutOpt)$@
	$(MT_EXE)
	@echo "Succesful make..."
	@echo "...$@ is ready to use."

$(DISK1_PROPAGATION_CHECK_A): $(DISK1_PROPAGATION_CHECK_O) $(CONSOLECOLORS_O) $(CONSOLEACTOR_O) $(COMMONACTORS_O) $(TIMER_O) $(TIMERCOL_O) $(TTREETOOLS_O) $(CANVASEXTRAS_O) $(CLUSTEROCCUPANCY_MODULE_O) $(TRAJMEAS_HISTOGRAM_FILLER_MODULE_O) $(FILTERCALIBRATION_MODULE_O)
	@printf "Compiling done, linking disk1PropagationCheck...\n"
	@$(LD) $(LDFLAGS) -Wall -Wshadow $^ $(LIBS) $(OutPutOpt)$@
	$(MT_EXE)
	@echo "Succesful make..."
	@echo "...$@ is ready to use."


# Utility obj files

$(CONSOLECOLORS_O): $(CONSOLECOLORS_S)
	@printf "Compiling utility: \"ConsoleColors\"...\n"
	@$(CXX) $(CXXFLAGS) $(LIBS) -c $< $(OutPutOpt)$@
	@printf "Done.\n"

$(CONSOLEACTOR_O): $(CONSOLEACTOR_S)
	@printf "Compiling utility: \"ConsoleActor\"...\n"
	@$(CXX) $(CXXFLAGS) $(LIBS) -c $< $(OutPutOpt)$@
	@printf "Done.\n"

$(COMMONACTORS_O): $(COMMONACTORS_S)
	@printf "Compiling utility: \"CommonActors\"...\n"
	@$(CXX) $(CXXFLAGS) $(LIBS) -c $< $(OutPutOpt)$@
	@printf "Done.\n"

$(TIMER_O): $(TIMER_S)
	@printf "Compiling utility: \"TimerColored\"...\n"
	@$(CXX) $(CXXFLAGS) $(LIBS) -c $< $(OutPutOpt)$@
	@printf "Done.\n"

$(TIMERCOL_O): $(TIMERCOL_S)
	@printf "Compiling utility: \"TimerColored\"...\n"
	@$(CXX) $(CXXFLAGS) $(LIBS) -c $< $(OutPutOpt)$@
	@printf "Done.\n"

$(TTREETOOLS_O): $(TTREETOOLS_S)
	@printf "Compiling utility: \"TTreeTools\"...\n"
	@$(CXX) $(CXXFLAGS) $(LIBS) -c $< $(OutPutOpt)$@
	@printf "Done.\n"

$(CANVASEXTRAS_O): $(CANVASEXTRAS_S)
	@printf "Compiling utility: \"CanvasExtras\"...\n"
	@$(CXX) $(CXXFLAGS) $(LIBS) -c $< $(OutPutOpt)$@
	@printf "Done.\n"

$(TRAJMEAS_HISTOGRAM_FILLER_MODULE_O): $(TRAJMEAS_HISTOGRAM_FILLER_MODULE_S)
	@printf "Compiling utility: \"TrajMeasHistogramFillerModule\"...\n"
	@$(CXX) $(CXXFLAGS) $(LIBS) -c $< $(OutPutOpt)$@
	@printf "Done.\n"

$(FILTERCALIBRATION_MODULE_O): $(FILTERCALIBRATION_MODULE_S)
	@printf "Compiling utility: \"FilterCalibrationModule\"...\n"
	@$(CXX) $(CXXFLAGS) $(LIBS) -c $< $(OutPutOpt)$@
	@printf "Done.\n"

$(COSMIC_TRAJMEAS_HISTOS_MODULE_O): $(COSMIC_TRAJMEAS_HISTOS_MODULE_S)
	@printf "Compiling utility: \"CosmicTrajMeasHistosModule\"...\n"
	@$(CXX) $(CXXFLAGS) $(LIBS) -c $< $(OutPutOpt)$@
	@printf "Done.\n"

$(CLUSTEROCCUPANCY_MODULE_O): $(CLUSTEROCCUPANCY_MODULE_S)
	@printf "Compiling utility: \"ClusterOccupancyModule\"...\n"
	@$(CXX) $(CXXFLAGS) $(LIBS) -c $< $(OutPutOpt)$@
	@printf "Done.\n"

###

$(EFFICIENCY_MAIN_O): $(EFFICIENCY_MAIN_S)  
	@printf "Compiling program: \"efficiency_main\"...\n"
	@$(CXX) $(CXXFLAGS) $(LIBS) -c $< $(OutPutOpt)$@
	@printf "Done.\n"

$(EFFICIENCY_MULTIHITMEAS_O): $(EFFICIENCY_MULTIHITMEAS_S)  
	@printf "Compiling program: \"efficiency_multiHitMeas\"...\n"
	@$(CXX) $(CXXFLAGS) $(LIBS) -c $< $(OutPutOpt)$@
	@printf "Done.\n"

$(EFFICIENCY_FILTERCALIBRATION_O): $(EFFICIENCY_FILTERCALIBRATION_S)
	@printf "Compiling program: \"efficiency_filterCalibration\"...\n"
	@$(CXX) $(CXXFLAGS) $(LIBS) -c $< $(OutPutOpt)$@
	@printf "Done.\n"

$(COSMIC_MUON_PLOTTER_O): $(COSMIC_MUON_PLOTTER_S)
	@printf "Compiling program: \"cosmicMuonPlotter\"...\n"
	@$(CXX) $(CXXFLAGS) $(LIBS) -c $< $(OutPutOpt)$@
	@printf "Done.\n"

$(MERGE_SIMHIT_PLOTS_O): $(MERGE_SIMHIT_PLOTS_S)
	@printf "Compiling program: \"mergeSimhitPlots\"...\n"
	@$(CXX) $(CXXFLAGS) $(LIBS) -c $< $(OutPutOpt)$@
	@printf "Done.\n"

$(DISK1_PROPAGATION_CHECK_O): $(DISK1_PROPAGATION_CHECK_S)
	@printf "Compiling program: \"disk1PropagationCheck\"...\n"
	@$(CXX) $(CXXFLAGS) $(LIBS) -c $< $(OutPutOpt)$@
	@printf "Done.\n"

clean:
	@rm -f $(OBJS) $(PROGRAMS) core

distclean: clean
	@rm -f $(PROGRAMS) *Dict.* *.def *.exp \
	*.root *.ps *.so *.lib *.dll *.d *.log .def so_locations
	@rm -rf cxx_repository

.SUFFIXES: .$(SrcSuf)
