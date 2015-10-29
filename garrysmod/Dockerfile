FROM inanimate/steamcmd-play

ENV GAME_NAME garrysmod
ENV GAME_ID 4020

ENV GAME_PATH ${STEAMCMD_LOC}/${GAME_NAME}

RUN ${STEAMCMD} +login anonymous +force_install_dir ${GAME_PATH} +app_update ${GAME_ID} validate +quit
RUN ${STEAMCMD} +login anonymous +force_install_dir ${GAME_PATH} +app_update ${GAME_ID} validate +quit

WORKDIR ${GAME_PATH}

ENTRYPOINT ["./srcds_run", "-game garrysmod"]

CMD ["+sv_lan", "0", "+map", "gm_construct"]
