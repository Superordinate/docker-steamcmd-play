FROM inanimate/steamcmd-play

ENV GAME_NAME tf
ENV GAME_ID 232250

ENV GAME_PATH ${STEAMCMD_LOC}/${GAME_NAME}

RUN ${STEAMCMD} +login anonymous +usetcp +tcp +force_install_dir ${GAME_PATH} +app_update ${GAME_ID} validate +quit
RUN ${STEAMCMD} +login anonymous +usetcp +tcp +force_install_dir ${GAME_PATH} +app_update ${GAME_ID} validate +quit


WORKDIR ${GAME_PATH}

ENTRYPOINT ["./srcds_run", "-game tf"]

CMD ["+sv_lan", "0", "+map", "ctf_2fort", "+sv_pure", "1"]
